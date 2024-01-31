# PHS-LLM: Real-time Multilingual Multiplatform Public Health Surveillance Pipeline using Large Language Models

BIS 687 Capstone Project @ Yale University

**link to the models**: TBA  
**link to the dataset**: TBA  

### News
[Jan 31, 2024] Feel free to contact xinyu[dot]zhou[at]yale[dot]edu if you're interested in collaborating on this project!

### Why is it important?
**One of the major gaps in social media inforveillance is the lack of real-time inforveillance.** 

The effectiveness of many public health interventions (such as social distancing, COVID-19 testing, and vaccination) relies on the public’s adherence [1, 2, 3]. Based on social media data, previous studies trained machine learning models to learn about sentiments towards public health interventions [1, 2, 3, 4]. For example, trajectories of sentiments can reveal how public adherence fluctuates due to policy changes. [1, 2, 3, 4] Also statistical analysis, such as fixed effect model and multiple regression, can reveal linkages between policy and sentiment [1, 3]. In addition, topic modeling can show the public’s top concerns [2]. These studies aspire to use streaming social media data to inform policymakers close to real time [1, 2, 3, 4]. However, researchers needed to annotate training data and train machine-learning models before implementing social media-based public health surveillance, because traditional machine-learning models are lacking in generalizability [1, 2, 3]. Currently, there’s a lack of real-time surveillance based on social media data [4] Such a gap leads to delays in evidence-based policy adjustments and may lead to population-level health consequences, such as failing to avert millions of preventable deaths [5]. 

### What do we want to do?
Large Language Models (LLMs) offer generalizability and can undertake tasks that they have never seen before. However, there are yet to be LLMs tailored for public health surveillance. In this study, we finetuned LLMs, specifically BLOOM-176B and BLOOM-7B, for generalizable public health surveillance that can be easily applied in low-resource settings [6]. We proposed a pipeline for real-time public health surveillance with LLMs, that can be integrated into existing public health surveillance systems to assist evidence-based policymaking. We designed a benchmark to evaluate models’ capability and flexibility for multilingual multiplatform social media inforveillance.

Using Flash attention-2 [7], DeepSpeed ZeRO Stage3 [8], and QLoRA [9], we can (continual pretrain and) instruction-based finetune LLMs, using existing social media datasets.
Based on the LLMs we pre-train (and ChatGPT API if needed), we can develop a real-time public health surveillance pipeline, where we (1) collect data from social media platforms using API (2) remove sensitive information from social media posts [10] (3) analyze de-identified data based on LLMs (4) provide the pipeline for exporting data for statistical analysis (5) provide pipelines for visualizing data using figures or websites.

### References:
[1] Zhou, Xinyu, et al. "Spatiotemporal trends in COVID-19 vaccine sentiments on a social media platform and correlations with reported vaccine coverage." Bulletin of the World Health Organization 102.1 (2024): 32.  
[2] Zhou, Xinyu, et al. "Comparison of public responses to containment measures during the initial outbreak and resurgence of COVID-19 in China: infodemiology study." Journal of medical Internet research 23.4 (2021): e26518.  
[3] Zhou, Xinyu, et al. "Deep Learning Analysis of COVID-19 Vaccine Hesitancy and Confidence Expressed on Twitter in 6 High-Income Countries: Longitudinal Observational Study." Journal of Medical Internet Research 25 (2023): e49753.  
[4] Tsao, Shu-Feng, et al. "What social media told us in the time of COVID-19: a scoping review." The Lancet Digital Health 3.3 (2021): e175-e194.  
[5] Cai, Jun, et al. "Modeling transmission of SARS-CoV-2 omicron in China." Nature medicine 28.7 (2022): 1468-1475.  
[6] Touvron, Hugo, et al. "Llama 2: Open foundation and fine-tuned chat models." arXiv preprint arXiv:2307.09288 (2023).  
[7] Dao, Tri. "Flashattention-2: Faster attention with better parallelism and work partitioning." arXiv preprint arXiv:2307.08691 (2023).  
[8] Aminabadi, Reza Yazdani, et al. "DeepSpeed-inference: enabling efficient inference of transformer models at unprecedented scale." SC22: International Conference for High Performance Computing, Networking, Storage and Analysis. IEEE, 2022.  
[9] Dettmers, Tim, et al. "Qlora: Efficient finetuning of quantized llms." arXiv preprint arXiv:2305.14314 (2023).  
[10] Norgeot, Beau, et al. "Protected Health Information filter (Philter): accurately and securely de-identifying free-text clinical notes." NPJ digital medicine 3.1 (2020): 57.  

