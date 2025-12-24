<script setup>
import frameworkImage from '@/assets/images/grape-lm-framework.png'
</script>
<template>
  <div class="flex flex-col items-center py-6 px-4">
    <div class="w-full max-w-3xl bg-white rounded-lg shadow-xl p-8 dark:bg-gray-900">
      <!-- 标题 -->
      <h1 class="text-4xl font-bold text-center text-gray-800 mb-2 dark:text-gray-400">GRAPE-LM</h1>
      <p class="text-center text-gray-500 mb-8">
        Generator of RNA Aptamers Powered by activity-guided Evolution and Language Model
      </p>

      <!-- 方法介绍 -->
      <div class="mb-4">
        <h2 class="text-2xl font-semibold text-gray-800 mb-4 dark:text-gray-400">Abstract</h2>
        <div class="prose max-w-none text-gray-700 dark:text-gray-500">
          <p class="mb-4 text-justify">
            The directed evolution of biomolecules is an iterative process. While advancements in
            language models have expedited protein evolution, effectively evolving RNA remains a
            challenge. RNA aptamers, selected for their binding properties, provide an ideal system
            to address this challenge, yet traditional aptamer discovery still relies on
            labor-intensive, multi-round screening. Here, we introduce GRAPE-LM<sup
              class="font-medium"
              >1</sup
            >
            (Generator of RNA Aptamers Powered by activity-guided Evolution and Language Model), a
            generative AI framework designed for the one-round evolution of RNA aptamers. GRAPE-LM
            integrates a Transformer-based conditional autoencoder with nucleic acid language
            models<sup class="font-medium">2-7</sup> and is guided by CRISPR/Cas-based aptamer
            screening data<sup class="font-medium">8</sup> derived from intracellular environments.
            We validate GRAPE-LM on three disparate targets: the human T-cell receptor CD3ε, the
            Receptor-Binding Domain (RBD) of the SARS-CoV-2 Spike protein, and the human oncogenic
            transcription factor c-Myc (an intracellular disordered protein). GRAPE-LM, informed
            with only a single round of CRISPR/Cas-based screening, successfully obtains RNA
            aptamers that outperform those driven from multiple rounds of human selection and
            optimization.
          </p>
          <div class="mb-4">
            <div class="bg-gray-50 p-4 rounded-lg dark:bg-gray-800">
              <img
                :src="frameworkImage"
                alt="GRAPE-LM Framework Diagram"
                class="w-full h-auto rounded-lg shadow-sm"
              />
              <p class="text-sm text-gray-500 mt-2 text-center italic">
                Overview of the GRAPE-LM framework for RNA aptamer evolution.
              </p>
            </div>
          </div>
        </div>
        <!-- <p class="">
          The method starts with user-provided seed sequences and iteratively generates new RNA
          aptamer candidates.
        </p> -->
      </div>

      <!-- 跳转按钮 -->
      <!-- <div class="text-center">
        <router-link
          to="/submit"
          class="inline-block px-8 py-3 bg-violet-600 text-white font-semibold rounded-lg shadow-md hover:bg-violet-700 focus:outline-none focus:ring-2 focus:ring-violet-500 focus:ring-opacity-75 transition transform hover:scale-105"
        >
          Start Generating Aptamers
        </router-link>
      </div> -->

      <!-- 参考文献 -->
      <div class="mt-10">
        <h2 class="text-2xl font-semibold text-gray-800 mb-4 dark:text-gray-400">References</h2>
        <div class="bg-gray-50 p-4 rounded-lg dark:bg-gray-800">
          <div class="space-y-3 text-sm text-justify text-gray-700 dark:text-gray-500">
            <div class="border-l-4 border-violet-500 pl-4">
              <p class="font-medium">
                <span class="font-bold">1. </span>Jun Zhang, Ju Zhang, Shaoxuan Tang, Chuancheng
                Liu, Yushan Cai, Hao Zeng, Xiangjie Meng, Bei Liu, Yang Zhang, Yu Wang. Single round
                evolution of RNA aptamers with GRAPE-LM.
              </p>
              <p class="text-gray-600 italic dark:text-gray-600">(Submitted).</p>
            </div>
            <!-- RNA-FM -->
            <div class="border-l-4 border-violet-500 pl-4">
              <p class="font-medium">
                <span class="font-bold">2. </span>Shen, T. et al. Accurate RNA 3D structure
                prediction using a language model-based deep learning approach.
              </p>
              <p class="text-gray-600 italic dark:text-gray-600">
                Nature Methods 21, 2287-2298 (2024).
              </p>
            </div>
            <!-- RNA-BERT -->
            <div class="border-l-4 border-violet-500 pl-4">
              <p class="font-medium">
                <span class="font-bold">3. </span>Akiyama, M. & Sakakibara, Y. Informative RNA base
                embedding for RNA structural alignment and clustering by deep representation
                learning.
              </p>
              <p class="text-gray-600 italic dark:text-gray-600">
                NAR Genomics and Bioinformatics 4, lqac012 (2022).
              </p>
            </div>
            <!-- RNAErnie -->
            <div class="border-l-4 border-violet-500 pl-4">
              <p class="font-medium">
                <span class="font-bold">4. </span>Wang, N. et al. Multi-purpose RNA language
                modelling with motif-aware pretraining and type-guided fine-tuning.
              </p>
              <p class="text-gray-600 italic dark:text-gray-600">
                Nature Machine Intelligence 6, 548-557 (2024).
              </p>
            </div>
            <!-- EvoFlow-RNA -->
            <div class="border-l-4 border-violet-500 pl-4">
              <p class="font-medium">
                <span class="font-bold">5. </span>Patel, S., Peng, F.Z., Fraser, K., Chatterjee, P.
                & Yao, S. EvoFlow-RNA: Generating and 1220 Representing non-coding RNA with a
                Language Model.
              </p>
              <p class="text-gray-600 italic dark:text-gray-600">
                bioRxiv, 2025.2002.2025.639942 1221 (2025).
              </p>
            </div>
            <!-- RiNALMo -->
            <div class="border-l-4 border-violet-500 pl-4">
              <p class="font-medium">
                <span class="font-bold">6. </span>Penić, R.J., Vlašić, T., Huber, R.G., Wan, Y. &
                Šikić, M. RiNALMo: general-purpose RNA language models can generalize well on
                structure prediction tasks.
              </p>
              <p class="text-gray-600 italic dark:text-gray-600">
                Nature Communications 16, 1224 5671 (2025).
              </p>
            </div>
            <!-- Evo -->
            <div class="border-l-4 border-violet-500 pl-4">
              <p class="font-medium">
                <span class="font-bold">7. </span>Nguyen, E. et al. Sequence modeling and design
                from molecular to genome scale with Evo.
              </p>
              <p class="text-gray-600 italic dark:text-gray-600">Science 386, eado9336 (2024).</p>
            </div>
            <!-- dataset -->
            <div class="border-l-4 border-violet-500 pl-4">
              <p class="font-medium">
                <span class="font-bold">8. </span>Zhang, J. et al. CRISmers NGS data used and
                generated by GRAPE-LM (1.0) [Data set].
              </p>
              <p class="text-gray-600 italic dark:text-gray-600">
                Zenodo (2025). https://doi.org/10.5281/zenodo.18005327
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
