# DeepSeek 

* DeepSeek - zero
* DeepSeek - R1

## Story of AI is a story about GPUs

* 2012 Imagenet competition - AlexNet
* 2017 transformers papers - Algorithm is about Attention and being parallell (mother board with 8 GPUs)
* 2020-2022 GPTS (Generative Pre-trained Transformer) - pre-trained models in parallel cluster
* 2025 - DeepSeek -> GPU efficiency

## Some Points (By Andrew Ng)

* A few important trends that have been happening in plain sight:
* (i) China is catching up to the U.S. in generative AI, with implications for the AI supply chain
* (ii) Open weight models  create opportunities for application builders
* (iii) Scaling up isn’t the only path to AI progress. Despite the massive focus on and hype around processing power, algorithmic innovations are rapidly pushing down training costs.
* About a week ago, DeepSeek, a company based in China, released DeepSeek-R1, a remarkable model whose performance on benchmarks is comparable to OpenAI’s o1.
* Further, it was released as an open weight model with a permissive MIT license.
* The share prices of Nvidia and a number of other U.S. tech companies plunged this week. (As of the time of writing, some have recovered somewhat.)
* Here’s what DeepSeek may have caused many people to realize:
* The world is catching up to the U.S. in generative AI.
* When ChatGPT was launched in November 2022, the U.S. was significantly ahead of China in generative AI.
* Impressions change slowly, and so even recently people thought China was behind.
* But in reality, this gap has rapidly eroded over the past two years.
* With models from China such as Qwen, Kimi, InternVL, and DeepSeek, China had clearly been closing the gap,
* and in areas such as video generation there were already moments where China seemed to be in the lead.
* Many are thrilled that DeepSeek-R1 was released as an open weight model, with a technical report that shares many details.
* In contrast, a number of U.S. companies have pushed for regulation to stifle open source by hyping up hypothetical AI dangers such as human extinction.
* It is now clear that open source/open weight models are a key part of the AI supply chain
* Many companies will use them: AWS, Azure, Hugginface, Dell, etc. 
* If the U.S. continues to slow down  open source, China will come to dominate this part of the supply chain
* By some extimates, OpenAI’s o1 costs $60 per million output tokens
* DeepSeek R1 costs $2.19 per million output tokens
* This nearly 30x difference brought the trend of falling prices to the attention of many people.


## GPUs and NVIDIA

* Article by Jeffrey Emanuel
* https://youtubetranscriptoptimizer.com/blog/05_the_short_case_for_nvda
* Key points:
* The Short Case for Nvidia Stock
*  Nvidia. It's not every day that a company goes from relative obscurity to being worth more
* than the combined stock markets of England, France, or Germany!
* NVIDIA in AI is key.
* Some scenarios
* The Bull Case:
* Nvidia has somehow ended up with something close to a monopoly in terms of the share of aggregate
*  industry capex that is spent on training and inference infrastructure.
*  Some of the largest and most profitable companies in the world, like Microsoft, Apple, Amazon, Meta, Google, Oracle, etc., have
* all decided that they must do and spend whatever it takes to stay competitive in this space because they simply cannot
* afford to be left behind.
* The amount of capex dollars, gigawatts of electricity used, square footage of new-build data centers, and, of course,
*  the number of GPUs, has absolutely exploded and seems to show no sign of slowing down.
*  And Nvidia is able to earn insanely high 90%+ gross margins on the most high-end, datacenter oriented products.
*  New Stargate project hopes to spend half a trillion in infrastructure. A data center is about $ 1.5 billion.
*  Let us ask DeepSeek-R1 (7b) how many data center this is
*  link
*  The New Paradigm:
*  What happens to the data center after you pre-trained lots of models. What do you use the aging data center for? 
*  Inference time compute 
*  the total amount of inference compute (measured in various ways, such as FLOPS, in GPU memory footprint, etc.)
*  was much, much less than what was required for the pre-training phase.
* With the advent of the revolutionary Chain-of-Thought ("COT") models introduced in the past year, most noticeably in
* OpenAI's flagship O1 model (but very recently in DeepSeek's new R1 model), all that changed.
* link - COT
* these new COT models also generate intermediate "logic tokens"; think of this as a sort of
* scratchpad or "internal monologue" of the model while it's trying to solve your problem or complete its assigned task.
* This represents a true sea change in how inference compute works: now, the more tokens you use for this
* internal chain of thought process, the better the quality of the final output you can provide the user.
* In effect, it's like giving a human worker more time and resources to accomplish a task, so they can double and triple check
* their work,
* It turns out that this approach (COT) works almost amazingly well
* By breaking the inference process into what is effectively many intermediate stages,
*  they can try lots of different things and see what's working and keep trying to course-correct and try other approaches
*  until they can reach a fairly high threshold of confidence
*  So, inference now is critical and is a different type of computing
*  But Why Should Nvidia Get to Capture All The Upside?
*  to really understand why Nvidia is currently capturing so much of the pie today.
*  After all, they aren't the only company that even makes GPUs. AMD makes respectable GPUs that,
*  on paper, have comparable numbers of transistors, which are made using similar process nodes, etc.
*  Sure, they aren't as fast or as advanced as Nvidia's GPUs, but it's not like the Nvidia GPUs are 10x faster or anything like that.
*  In fact, in terms of naive/raw dollars per FLOP, AMD GPUs are something like half the price of Nvidia GPUs.
*  Looking at other semiconductor markets such as the DRAM market, despite the fact that it is also very highly consolidated
*  with only 3 meaningful global players (Samsung, Micron, SK-Hynix), gross margins in the DRAM market range from negative
*  at the bottom of the cycle to ~60% at the very top of the cycle, with an average in the 20% range.
*  Compare that to Nvidia's overall gross margin in recent quarters of ~75%
*  the main reasons have to do with software— better drivers that "just work" on Linux and which are highly
*  battle-tested and reliable (unlike AMD, which is notorious for the low quality and instability of their Linux drivers),
*  and highly optimized open-source code in popular libraries such as PyTorch that has been tuned to work really well on Nvidia GPUs.
*  It goes beyond that though— the very programming framework that coders use to write low-level code that is optimized
*  for GPUs, CUDA, is totally proprietary to Nvidia, and it has become a de facto standard.
*  If you want to hire a bunch of extremely talented programmers who know how to make things go really fast on GPUs,
*  and pay them $650k/year or whatever the going rate is for people with that particular expertise,
*  chances are that they are going to "think" and work in CUDA.
*  <think>
*  Besides software superiority
*  </think>
* the other major thing that Nvidia has going for it is what is known as interconnect— essentially,
* the bandwidth that connects together thousands of GPUs together efficiently so they can be jointly harnessed to train
* today's leading-edge foundational models.
* In short, the key to efficient training is to keep all the GPUs as fully utilized as possible all the time— not
* waiting around idling until they receive the next chunk of data they need to compute the next step of the training process.
* The bandwidth requirements are extremely high— much, much higher than the typical bandwidth that is needed in 
* traditional data center use cases.
* Nvidia made an incredibly smart decision to purchase the Israeli company Mellanox back in 2019 for a mere $6.9b,
* and this acquisition is what provided them with their industry leading interconnect technology.
* Note that interconnect speed is a lot more relevant to the training process, where you have to harness together the
* output of thousands of GPUs at the same time, than the inference process (including COT inference),
* which can use just a handful of GPUs—
* all you need is enough VRAM to store the quantized (compressed) model weights of the already-trained model.
* The Major Threats
* After chatGPT, Suddenly, big companies were ready to spend many, many billions of dollars incredibly quickly.
* NVIDIA was positined perfectly for it
* The Hardware Level Threat
* Several new chip makers in the horizon (Cerebras, Groq, Google, which has been developing its own proprietary TPUs , etc.)
* How should one think about the future of this business when literally every single one of NVIDIA's VIP customers is
*  building their own custom chips specifically for AI training and inference?
*  When thinking about all this, you should keep one incredibly important thing in mind: Nvidia is largely an IP based company.
*  They don't make their own chips.
*  The true special sauce for making these incredible devices arguably comes more from TSMC,
*  the actual fab, and ASML, which makes the special EUV lithography machines used by
*  TSMC to make these leading-edge process node chips.
*  As much as senior chip designers at Nvidia earn per year, surely some of the best of them could be lured away
*  by these other tech behemoths for enough cash and stock.
*  And once they have a team and resources, they can design innovative chips (again, perhaps not
*  even 50% as advanced as an H100, but with that Nvidia gross margin, there is plenty of room to work with) in 2 to 3 years,
*  and thanks for TSMC, they can turn those into actual silicon using the exact same process node technology as Nvidia.

The Software Threat

As if these looming hardware threats weren't bad enough, there are a few developments in the software world in the last couple years that, while they started out slowly, are now picking up real steam and could pose a serious threat to the software dominance of Nvidia's CUDA. The first of these is the horrible Linux drivers for AMD GPUs. Remember we talked about how AMD has inexplicably allowed these drivers to suck for years despite leaving massive amounts of money on the table?

Well, amusingly enough, the infamous hacker George Hotz (famous for jailbreaking the original iphone as a teenager, and currently the CEO of self-driving startup Comma.ai and AI computer company Tiny Corp, which also makes the open-source tinygrad AI software framework), recently announced that he was sick and tired of dealing with AMD's bad drivers, and desperately wanted to be able to to leverage the lower cost AMD GPUs in their TinyBox AI computers (which come in multiple flavors, some of which use Nvidia GPUs, and some of which use AMD GPUS).

Well, he is making his own custom drivers and software stack for AMD GPUs without any help from AMD themselves; on Jan. 15th of 2025, he tweeted via his company's X account that "We are one piece away from a completely sovereign stack on AMD, the RDNA3 assembler. We have our own driver, runtime, libraries, and emulator. (all in ~12,000 lines!)" Given his track record and skills, it is likely that they will have this all working in the next couple months, and this would allow for a lot of exciting possibilities of using AMD GPUs for all sorts of applications where companies currently feel compelled to pay up for Nvidia GPUs.

OK, well that's just a driver for AMD, and it's not even done yet. What else is there? Well, there are a few other areas on the software side that are a lot more impactful. For one, there is now a massive concerted effort across many large tech companies and the open source software community at large to make more generic AI software frameworks that have CUDA as just one of many "compilation targets".

That is, you write your software using higher-level abstractions, and the system itself can automatically turn those high-level constructs into super well-tuned low-level code that works extremely well on CUDA. But because it's done at this higher level of abstraction, it can just as easily get compiled into low-level code that works extremely well on lots of other GPUs and TPUs from a variety of providers, such as the massive number of custom chips in the pipeline from every big tech company.

The most famous examples of these frameworks are MLX (sponsored primarily by Apple), Triton (sponsored primarily by OpenAI), and JAX (developed by Google). MLX is particularly interesting because it provides a PyTorch-like API that can run efficiently on Apple Silicon, showing how these abstraction layers can enable AI workloads to run on completely different architectures. Triton, meanwhile, has become increasingly popular as it allows developers to write high-performance code that can be compiled to run on various hardware targets without having to understand the low-level details of each platform.

These frameworks allow developers to write their code once using high powered abstractions and then target tons of platforms automatically— doesn't that sound like a better way to do things, which would give you a lot more flexibility in terms of how you actually run the code?

In the 1980s, all the most popular, best selling software was written in hand-tuned assembly language. The PKZIP compression utility for example was hand crafted to maximize speed, to the point where a competently coded version written in the standard C programming language and compiled using the best available optimizing compilers at the time, would run at probably half the speed of the hand-tuned assembly code. The same is true for other popular software packages like WordStar, VisiCalc, and so on.

Over time, compilers kept getting better and better, and every time the CPU architectures changed (say, from Intel releasing the 486, then the Pentium, and so on), that hand-rolled assembler would often have to be thrown out and rewritten, something that only the smartest coders were capable of (sort of like how CUDA experts are on a different level in the job market versus a "regular" software developer). Eventually, things converged so that the speed benefits of hand-rolled assembly were outweighed dramatically by the flexibility of being able to write code in a high-level language like C or C++, where you rely on the compiler to make things run really optimally on the given CPU.

Nowadays, very little new code is written in assembly. I believe a similar transformation will end up happening for AI training and inference code, for similar reasons: computers are good at optimization, and flexibility and speed of development is increasingly the more important factor— especially if it also allows you to save dramatically on your hardware bill because you don't need to keep paying the "CUDA tax" that gives Nvidia 90%+ margins.

Yet another area where you might see things change dramatically is that CUDA might very well end up being more of a high level abstraction itself— a "specification language" similar to Verilog (used as the industry standard to describe chip layouts) that skilled developers can use to describe high-level algorithms that involve massive parallelism (since they are already familiar with it, it's very well constructed, it's the lingua franca, etc.), but then instead of having that code compiled for use on Nvidia GPUs like you would normally do, it can instead be fed as source code into an LLM which can port it into whatever low-level code is understood by the new Cerebras chip, or the new Amazon Trainium2, or the new Google TPUv6, etc. This isn't as far off as you might think; it's probably already well within reach using OpenAI's latest O3 model, and surely will be possible generally within a year or two.

The Theoretical Threat

Perhaps the most shocking development which was alluded to earlier happened in the last couple of weeks. And that is the news that has totally rocked the AI world, and which has been dominating the discourse among knowledgeable people on Twitter despite its complete absence from any of the mainstream media outlets: that a small Chinese startup called DeepSeek released two new models that have basically world-competitive performance levels on par with the best models from OpenAI and Anthropic (blowing past the Meta Llama3 models and other smaller open source model players such as Mistral). These models are called DeepSeek-V3 (basically their answer to GPT-4o and Claude3.5 Sonnet) and DeepSeek-R1 (basically their answer to OpenAI's O1 model).

Why is this all so shocking? Well, first of all, DeepSeek is a tiny Chinese company that reportedly has under 200 employees. The story goes that they started out as a quant trading hedge fund similar to TwoSigma or RenTec, but after Xi Jinping cracked down on that space, they used their math and engineering chops to pivot into AI research. Who knows if any of that is really true or if they are merely some kind of front for the CCP or the Chinese military. But the fact remains that they have released two incredibly detailed technical reports, for DeepSeek-V3 and DeepSeekR1.

These are heavy technical reports, and if you don't know a lot of linear algebra, you probably won't understand much. But what you should really try is to download the free DeepSeek app on the AppStore here and install it using a Google account to log in and give it a try (you can also install it on Android here), or simply try it out on your desktop computer in the browser here. Make sure to select the "DeepThink" option to enable chain-of-thought (the R1 model) and ask it to explain parts of the technical reports in simple terms.

This will simultaneously show you a few important things:

One, this model is absolutely legit. There is a lot of BS that goes on with AI benchmarks, which are routinely gamed so that models appear to perform great on the benchmarks but then suck in real world tests. Google is certainly the worst offender in this regard, constantly crowing about how amazing their LLMs are, when they are so awful in any real world test that they can't even reliably accomplish the simplest possible tasks, let alone challenging coding tasks. These DeepSeek models are not like that— the responses are coherent, compelling, and absolutely on the same level as those from OpenAI and Anthropic.

Two, that DeepSeek has made profound advancements not just in model quality, but more importantly in model training and inference efficiency. By being extremely close to the hardware and by layering together a handful of distinct, very clever optimizations, DeepSeek was able to train these incredible models using GPUs in a dramatically more efficient way. By some measurements, over ~45x more efficiently than other leading-edge models. DeepSeek claims that the complete cost to train DeepSeek-V3 was just over $5mm. That is absolutely nothing by the standards of OpenAI, Anthropic, etc., which were well into the $100mm+ level for training costs for a single model as early as 2024.

How in the world could this be possible? How could this little Chinese company completely upstage all the smartest minds at our leading AI labs, which have 100 times more resources, headcount, payroll, capital, GPUs, etc? Wasn't China supposed to be crippled by Biden's restriction on GPU exports? Well, the details are fairly technical, but we can at least describe them at a high level. It might have just turned out that the relative GPU processing poverty of DeepSeek was the critical ingredient to make them more creative and clever, necessity being the mother of invention and all.

A major innovation is their sophisticated mixed-precision training framework that lets them use 8-bit floating point numbers (FP8) throughout the entire training process. Most Western AI labs train using "full precision" 32-bit numbers (this basically specifies the number of gradations possible in describing the output of an artificial neuron; 8 bits in FP8 lets you store a much wider range of numbers than you might expect— it's not just limited to 256 different equal-sized magnitudes like you'd get with regular integers, but instead uses clever math tricks to store both very small and very large numbers— though naturally with less precision than you'd get with 32 bits.) The main tradeoff is that while FP32 can store numbers with incredible precision across an enormous range, FP8 sacrifices some of that precision to save memory and boost performance, while still maintaining enough accuracy for many AI workloads.

DeepSeek cracked this problem by developing a clever system that breaks numbers into small tiles for activations and blocks for weights, and strategically uses high-precision calculations at key points in the network. Unlike other labs that train in high precision and then compress later (losing some quality in the process), DeepSeek's native FP8 approach means they get the massive memory savings without compromising performance. When you're training across thousands of GPUs, this dramatic reduction in memory requirements per GPU translates into needing far fewer GPUs overall.

Another major breakthrough is their multi-token prediction system. Most Transformer based LLM models do inference by predicting the next token— one token at a time. DeepSeek figured out how to predict multiple tokens while maintaining the quality you'd get from single-token prediction. Their approach achieves about 85-90% accuracy on these additional token predictions, which effectively doubles inference speed without sacrificing much quality. The clever part is they maintain the complete causal chain of predictions, so the model isn't just guessing— it's making structured, contextual predictions.

One of their most innovative developments is what they call Multi-head Latent Attention (MLA). This is a breakthrough in how they handle what are called the Key-Value indices, which are basically how individual tokens are represented in the attention mechanism within the Transformer architecture. Although this is getting a bit too advanced in technical terms, suffice it to say that these KV indices are some of the major uses of VRAM during the training and inference process, and part of the reason why you need to use thousands of GPUs at the same time to train these models— each GPU has a maximum of 96 gb of VRAM, and these indices eat that memory up for breakfast.

Their MLA system finds a way to store a compressed version of these indices that captures the essential information while using far less memory. The brilliant part is this compression is built directly into how the model learns— it's not some separate step they need to do, it's built directly into the end-to-end training pipeline. This means that the entire mechanism is "differentiable" and able to be trained directly using the standard optimizers. All this stuff works because these models are ultimately finding much lower-dimensional representations of the underlying data than the so-called "ambient dimensions". So it's wasteful to store the full KV indices, even though that is basically what everyone else does.

Not only do you end up wasting tons of space by storing way more numbers than you need, which gives a massive boost to the training memory footprint and efficiency (again, slashing the number of GPUs you need to train a world class model), but it can actually end up improving model quality because it can act like a "regularizer," forcing the model to pay attention to the truly important stuff instead of using the wasted capacity to fit to noise in the training data. So not only do you save a ton of memory, but the model might even perform better. At the very least, you don't get a massive hit to performance in exchange for the huge memory savings, which is generally the kind of tradeoff you are faced with in AI training.

They also made major advances in GPU communication efficiency through their DualPipe algorithm and custom communication kernels. This system intelligently overlaps computation and communication, carefully balancing GPU resources between these tasks. They only need about 20 of their GPUs' streaming multiprocessors (SMs) for communication, leaving the rest free for computation. The result is much higher GPU utilization than typical training setups achieve.

Another very smart thing they did is to use what is known as a Mixture-of-Experts (MOE) Transformer architecture, but with key innovations around load balancing. As you might know, the size or capacity of an AI model is often measured in terms of the number of parameters the model contains. A parameter is just a number that stores some attribute of the model; either the "weight" or importance a particular artificial neuron has relative to another one, or the importance of a particular token depending on its context (in the "attention mechanism"), etc.

Meta's latest Llama3 models come in a few sizes, for example: a 1 billion parameter version (the smallest), a 70B parameter model (the most commonly deployed one), and even a massive 405B parameter model. This largest model is of limited utility for most users because you would need to have tens of thousands of dollars worth of GPUs in your computer just to run at tolerable speeds for inference, at least if you deployed it in the naive full-precision version. Therefore most of the real-world usage and excitement surrounding these open source models is at the 8B parameter or highly quantized 70B parameter level, since that's what can fit in a consumer-grade Nvidia 4090 GPU, which you can buy now for under $1,000.

So why does any of this matter? Well, in a sense, the parameter count and precision tells you something about how much raw information or data the model has stored internally. Note that I'm not talking about reasoning ability, or the model's "IQ" if you will: it turns out that models with even surprisingly modest parameter counts can show remarkable cognitive performance when it comes to solving complex logic problems, proving theorems in plane geometry, SAT math problems, etc.

But those small models aren't going to be able to necessarily tell you every aspect of every plot twist in every single novel by Stendhal, whereas the really big models can potentially do that. The "cost" of that extreme level of knowledge is that the models become very unwieldy both to train and to do inference on, because you always need to store every single one of those 405B parameters (or whatever the parameter count is) in the GPU's VRAM at the same time in order to do any inference with the model.

The beauty of the MOE model approach is that you can decompose the big model into a collection of smaller models that each know different, non-overlapping (at least fully) pieces of knowledge. DeepSeek's innovation here was developing what they call an "auxiliary-loss-free" load balancing strategy that maintains efficient expert utilization without the usual performance degradation that comes from load balancing. Then, depending on the nature of the inference request, you can intelligently route the inference to the "expert" models within that collection of smaller models that are most able to answer that question or solve that task.

You can loosely think of it as being a committee of experts who have their own specialized knowledge domains: one might be a legal expert, the other a computer science expert, the other a business strategy expert. So if a question comes in about linear algebra, you don't give it to the legal expert. This is of course a very loose analogy and it doesn't actually work like this in practice.

The real advantage of this approach is that it allows the model to contain a huge amount of knowledge without being very unwieldy, because even though the aggregate number of parameters is high across all the experts, only a small subset of these parameters is "active" at any given time, which means that you only need to store this small subset of weights in VRAM in order to do inference. In the case of DeepSeek-V3, they have an absolutely massive MOE model with 671B parameters, so it's much bigger than even the largest Llama3 model, but only 37B of these parameters are active at any given time— enough to fit in the VRAM of two consumer-grade Nvidia 4090 GPUs (under $2,000 total cost), rather than requiring one or more H100 GPUs which cost something like $40k each.

It's rumored that both ChatGPT and Claude use an MoE architecture, with some leaks suggesting that GPT-4 had a total of 1.8 trillion parameters split across 8 models containing 220 billion parameters each. Despite that being a lot more doable than trying to fit all 1.8 trillion parameters in VRAM, it still requires multiple H100-grade GPUs just to run the model because of the massive amount of memory used.

Beyond what has already been described, the technical papers mention several other key optimizations. These include their extremely memory-efficient training framework that avoids tensor parallelism, recomputes certain operations during backpropagation instead of storing them, and shares parameters between the main model and auxiliary prediction modules. The sum total of all these innovations, when layered together, has led to the ~45x efficiency improvement numbers that have been tossed around online, and I am perfectly willing to believe these are in the right ballpark.

One very strong indicator that it's true is the cost of DeepSeek's API: despite this nearly best-in-class model performance, DeepSeek charges something like 95% less money for inference requests via its API than comparable models from OpenAI and Anthropic. In a sense, it's sort of like comparing Nvidia's GPUs to the new custom chips from competitors: even if they aren't quite as good, the value for money is so much better that it can still be a no-brainer depending on the application, as long as you can qualify the performance level and prove that it's good enough for your requirements and the API availability and latency is good enough (thus far, people have been amazed at how well DeepSeek's infrastructure has held up despite the truly incredible surge of demand owing to the performance of these new models).

But unlike the case of Nvidia, where the cost differential is the result of them earning monopoly gross margins of 90%+ on their data-center products, the cost differential of the DeepSeek API relative to the OpenAI and Anthropic API could be simply that they are nearly 50x more compute efficient (it might even be significantly more than that on the inference side— the ~45x efficiency was on the training side). Indeed, it's not even clear that OpenAI and Anthropic are making great margins on their API services— they might be more interested in revenue growth and gathering more data from analyzing all the API requests they receive.

Before moving on, I'd be remiss if I didn't mention that many people are speculating that DeepSeek is simply lying about the number of GPUs and GPU hours spent training these models because they actually possess far more H100s than they are supposed to have given the export restrictions on these cards, and they don't want to cause trouble for themselves or hurt their chances of acquiring more of these cards. While it's certainly possible, I think it's more likely that they are telling the truth, and that they have simply been able to achieve these incredible results by being extremely clever and creative in their approach to training and inference. They explain how they are doing things, and I suspect that it's only a matter of time before their results are widely replicated and confirmed by other researchers at various other labs.

A Model That Can Really Think

The newer R1 model and technical report might even be even more mind blowing, since they were able to beat Anthropic to Chain-of-thought and now are basically the only ones besides OpenAI who have made this technology work at scale. But note that the O1 preview model was only released by OpenAI in mid-September of 2024. That's only ~4 months ago! Something you absolutely must keep in mind is that, unlike OpenAI, which is incredibly secretive about how these models really work at a low level, and won't release the actual model weights to anyone besides partners like Microsoft and other who sign heavy-duty NDAs, these DeepSeek models are both completely open-source and permissively licensed. They have released extremely detailed technical reports explaining how they work, as well as the code that anyone can look at and try to copy.

With R1, DeepSeek essentially cracked one of the holy grails of AI: getting models to reason step-by-step without relying on massive supervised datasets. Their DeepSeek-R1-Zero experiment showed something remarkable: using pure reinforcement learning with carefully crafted reward functions, they managed to get models to develop sophisticated reasoning capabilities completely autonomously. This wasn't just about solving problems— the model organically learned to generate long chains of thought, self-verify its work, and allocate more computation time to harder problems.

The technical breakthrough here was their novel approach to reward modeling. Rather than using complex neural reward models that can lead to "reward hacking" (where the model finds bogus ways to boost their rewards that don't actually lead to better real-world model performance), they developed a clever rule-based system that combines accuracy rewards (verifying final answers) with format rewards (encouraging structured thinking). This simpler approach turned out to be more robust and scalable than the process-based reward models that others have tried.

What's particularly fascinating is that during training, they observed what they called an "aha moment," a phase where the model spontaneously learned to revise its thinking process mid-stream when encountering uncertainty. This emergent behavior wasn't explicitly programmed; it arose naturally from the interaction between the model and the reinforcement learning environment. The model would literally stop itself, flag potential issues in its reasoning, and restart with a different approach, all without being explicitly trained to do this.

The full R1 model built on these insights by introducing what they call "cold-start" data— a small set of high-quality examples— before applying their RL techniques. They also solved one of the major challenges in reasoning models: language consistency. Previous attempts at chain-of-thought reasoning often resulted in models mixing languages or producing incoherent outputs. DeepSeek solved this through a clever language consistency reward during RL training, trading off a small performance hit for much more readable and consistent outputs.

The results are mind-boggling: on AIME 2024, one of the most challenging high school math competitions, R1 achieved 79.8% accuracy, matching OpenAI's O1 model. On MATH-500, it hit 97.3%, and it achieved the 96.3 percentile on Codeforces programming competitions. But perhaps most impressively, they managed to distill these capabilities down to much smaller models: their 14B parameter version outperforms many models several times its size, suggesting that reasoning ability isn't just about raw parameter count but about how you train the model to process information.

* The Fallout
* The recent scuttlebutt on Twitter and Blind (a corporate rumor website) is that these models caught Meta completely off guard and that they perform better than the new Llama4 models which are still being trained.
* Apparently, the Llama project within Meta has attracted a lot of attention internally from high-ranking technical executives,
* and as a result they have something like 13 individuals working on the Llama stuff who each individually earn more per year in total compensation than the combined training cost for the DeepSeek-V3 models which outperform it.
* How do you explain that to Zuck with a straight face? How does Zuck keep smiling while shoveling multiple billions of dollars to Nvidia to buy 100k H100s when a better model was trained using just 2k H100s for a bit over $5mm?
* But you better believe that Meta and every other big AI lab is taking these DeepSeek models apart,
* studying every word in those technical reports and every line of the open source
* code they released, trying desperately to integrate these same tric
* ks and optimizations into their own training and inference pipelin
* es. So what's the impact of all that? Well, naively it sort of seems like
* the aggregate demand for training and inference compute should be divided by some big number.
* Maybe not by 45, but maybe by 25 or even 30? Because whatever you thought you needed before these model releases, it's now a lot less.
* Now, an optimist might say "You are talking about a mere constant of proportionality,
*  a single multip e.
*  When you're dealing with an exponential growth curve, that stuff gets washed out so quickly
*   that it doesn't end up matter all that much."
* Wrapping it All Up
* At a high level, NVIDIA faces an unprecedented convergence of competitive threats that make its premium
* valuation increasingly difficult to justify
*  The company's supposed moats in hardware, software, and efficiency are all showing concerning cracks.
*  The whole world— thousands of the smartest people on the planet, backed by untold billions
*  of dollars of capital resources— are trying to assail them from every angle.
*  On the hardware front, innovative architectures from Cerebras and Groq demonstrate that NVIDIA's interconnect
*  advantage— a cornerstone of its data center dominance— can be circumvented through radical redesigns.
*  Cerebras' wafer-scale chips and Groq's deterministic compute approach deliver compelling
*  performance without needing NVIDIA's complex interconnect solutions.
*  More traditionally, every major NVIDIA customer (Google, Amazon, Microsoft, Meta, Apple) is developing custom
*  silicon that could chip away at high-margin data center revenue.
*  These aren't experimental projects anymore— Amazon alone is building out massive infrastructure
*   with over 400,000 custom chips for Anthropic.
*   The software moat appears equally vulnerable.
*   New high-level frameworks like MLX, Triton, and JAX are abstracting away CUDA's importance, while efforts to improve
*   AMD drivers could unlock much cheaper hardware alternatives.
*   The trend toward higher-level abstractions mirrors how assembly language gave way to C/C++, suggesting CUDA's
*   dominance may be more temporary than assumed.
*   Most importantly, we're seeing the emergence of LLM-powered code translation that could automatically
*   port CUDA code to run on any hardware target, potentially eliminating one of NVIDIA's strongest lock-in effects.
*   Perhaps most devastating is DeepSeek's recent efficiency breakthrough, achieving comparable model performance
*   at approximately 1/45th the compute cost.
*   This suggests the entire industry has been massively over-provisioning compute resources.
*   Combined with the emergence of more efficient inference architectures through chain-of-thought models,
*   the aggregate demand for compute could be significantly lower than current projections assume.
*    The economics here are compelling: when DeepSeek can match GPT-4 level performance while charging 95% less for API calls,
*     it suggests either NVIDIA's customers are burning cash unnecessarily or margins must come down dramatically.
* The fact that TSMC will manufacture competitive chips for any well-funded customer puts a natural
* ceiling on NVIDIA's architectural advantages.
* But more fundamentally, history shows that markets eventually find a way around artificial bottlenecks
* that generate super-normal profits.
* When layered together, these threats suggest NVIDIA faces a much rockier path to maintaining its current
* growth trajectory and margins than its valuation implies.
*  With five distinct vectors of attack— architectural innovation, customer vertical integration, software abstraction,
*  efficiency breakthroughs, and manufacturing democratization— the probability that at least one succeeds
*  in meaningfully impacting NVIDIA's margins or growth rate seems high.
*  

## DeepSeek papers

* https://arxiv.org/pdf/2402.03300
* https://arxiv.org/pdf/2501.12948
* https://arxiv.org/pdf/2201.11903
* 



## DeepSeek links

* https://github.com/deepseek-ai/DeepSeek-R1/tree/main
* https://trite-song-d6a.notion.site/Deepseek-R1-for-Everyone-1860af77bef3806c9db5e5c2a256577d
* https://unsloth.ai/blog/deepseekr1-dynamic
* https://github.com/Jiayi-Pan/TinyZero
* GitHub - huggingface/open-r1: Fully open reproduction of DeepSeek-R1
* https://github.com/huggingface/open-r1

## Hugging Face TRL

* https://github.com/huggingface/trl


## PTX

* https://docs.nvidia.com/cuda/pdf/ptx_isa_8.7.pdf

## Ollama

* [link](https://ollama.com/library/deepseek-r1)
* For a standard mac I ran deepseek-7b (7 billion parameters)

## Local GPU ( If your company needs it )

* By Matthew carrigan 
* to run the larger models such as the 671b you need a powerful computer or the cloud
* for about $ 6,000 you can build your GPU powerful enough to run DeepSeek-R1
* $ 6,000 obviously buys you a lot of Cloud Computing time
* Complete hardware + software setup for running Deepseek-R1 locally.
* The actual model, no distillations, and Q8 quantization for full quality.
* Total cost, $6,000.
* Motherboard: Gigabyte MZ73-LM0 or MZ73-LM1.
* We want 2 EPYC sockets to get a massive 24 channels of DDR5 RAM to max out that memory size and bandwidth.
* https://t.co/GCYsoYaKvZ
* CPU: 2x any AMD EPYC 9004 or 9005 CPU.
* LLM generation is bottlenecked by memory bandwidth, so you don't need a top-end one.
* Get the 9115 or even the 9015 if you really want to cut costs
* https://www.newegg.com/p/N82E16819113865
* RAM: This is the big one. We are going to need 768GB (to fit the model) across 24 RAM channels
* (to get the bandwidth to run it fast enough). That means 24 x 32GB DDR5-RDIMM modules.
* Example kits
* https://v-color.net/products/ddr5-ecc-rdimm-servermemory?variant=44758742794407
* https://www.newegg.com/nemix-ram-384gb/p/1X5-003Z-01FM7
* Case: You can fit this in a standard tower case, but make sure it has screw mounts
*  for a full server motherboard, which most consumer cases won't.
*  The Enthoo Pro 2 Server will take this motherboard:
*  https://t.co/m1KoTor49h
*  PSU: The power use of this system is surprisingly low! (<400W)
*  However, you will need lots of CPU power cables for 2 EPYC CPUs.
*  The Corsair HX1000i has enough, but you might be able to find a cheaper option:
*  https://www.corsair.com/us/en/p/psu/cp-9020259-na/hx1000i-fully-modular-ultra-low-noise-platinum-atx-1000-watt-pc-power-supply-cp-9020259-na
* heatsink: This is a tricky bit.
* AMD EPYC is socket SP5, and most heatsinks for SP5 assume you have a 2U/4U server blade,
* which we don't for this build.
* https://www.ebay.com/itm/226499280220
* And if you find the fans that come with that heatsink noisy,
* replacing with 1 or 2 of these per heatsink instead will be efficient and whisper-quiet:
* https://t.co/CaEwtoxRZj
* the SSD: Any 1TB or larger SSD that can fit R1 is fine.
*  recommend NVMe, just because you'll have to copy 700GB into RAM when you start the mode
*  And that's your system!
*  Put it all together and throw Linux on it.
*  Also, an important tip: Go into the BIOS and set the number of NUMA groups to 0.
*  This will ensure that every layer of the model is interleaved across all RAM chips, doubling our throughput.
*  Don't forget!
*  Now, software. Follow the instructions here to install llama.cpp
*  https://github.com/ggerganov/llama.cpp
*  ext, the model.
*  Time to download 700 gigabytes of weights from @huggingface!
*  Grab every file in the Q8_0 folder here:
*  https://t.co/9ni1Miw73O
*  Believe it or not, you're almost done. There are more elegant ways to set it up, but for a quick demo,
*  just do this.
*  llama-cli -m ./DeepSeek-R1.Q8_0-00001-of-00015.gguf --temp 0.6 -no-cnv -c 16384 -p "<｜User｜>How many Rs are there in strawberry?<｜Assistant｜>"
*  If all goes well, you should witness a short load period followed by the stream
*  of consciousness as a state-of-the-art local LLM begins to ponder your question:
*  And once it passes that test, just use llama-server to host the model and pass requests in from
*  your other software.
*  You now have frontier-level intelligence hosted entirely on your local machine, all open-source and free to use!
*  and if you got this far: Yes, there's no GPU in this build!
*  If you want to host on GPU for faster generation speed, you can! which will probably cost $100k+
*  the generation speed on this build is 6 to 8 tokens per second, depending on the specific CPU and RAM speed
*  you get, or slightly less if you have a long chat history.


## Code and logic

* https://github.com/rcalix1/TransferLearning/blob/main/ChainOfThought/AdvancedDeepLearning/DeepSeekPaperIdeas.ipynb

## GRPO

![shannon1](GRPO1.jpg)

![shannon2](GRPO2.jpg)

![shannon3](GRPO3.jpg)
