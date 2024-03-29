本库为 [KG 笔记法](https://forum-zh.obsidian.md/t/topic/2059)（Knowledge Graph Notes）的示例库。本库将说明 KG 笔记法的诞生以及基本使用。目前我已使用该方法搭建了百万字级的个人知识库。体验完整功能，需要配合 [path-finder](https://github.com/jerrywcy/obsidian-path-finder) 插件使用（本示例库已内置）。

# 一、简介

## 1. 源起：我们需要的究竟是什么？

相信很多人和过去的我一样，疑惑着究竟应该怎样使用笔记软件，或者说笔记能够给我们带来什么。

自从折腾笔记以来，这个问题就一直困扰着我。我曾寄希望于笔记软件，希望软件能够告诉我答案。于是在过去几年里，我陆陆续续换用了不同的笔记软件——印象笔记、OneNote、Notion、RoamResearch、Obsidian。每个软件都告诉我，应该构建自己的第二大脑，应该从笔记中产生新的洞见。但这怎么实现呢？软件没有告诉我答案。

于是，我认为这是方法论上的问题，从而将目光转向了各种笔记方法，希望这些方法能够让我的笔记软件变成我的第二大脑，让我能从笔记中产生新的灵感。从最原始的卢曼笔记盒，到衍生的 Zettlekasten，再到后来基于卡片盒的一系列方法，我把这些方法挨个用了一遍。比起笔记软件本身来说，这些方法确实在教我如何管理自己的笔记，以及如何从笔记中获取新的想法。但我仍觉得有些隔靴搔痒，因为这些方法更侧重于传递思想，而并没有给出可以构建个人笔记体系的严格步骤——它们更多地是在告诉我为什么要这么做（Why）以及这么做的愿景（Vision）。当我想了解如何构建自己的知识体系时，它们总是告诉我：“每个人的知识体系都是不同的，你不能照抄我，而是要参悟我的思想，构建自己的体系”。然而参悟了半年，我也没搞出个所以然。于是，我开始寻找更科学的方法。

兜兜转转，在 2020 年，我接触到了认知心理学、图书馆学和信息组织学。从那时起，我开始在前人研究结论的基础上，以一个更专业的角度来审视这个问题。

在阅读了一系列专业书籍后，我终于理解了做笔记的本质目的，那就是组织个人知识以方便所需时快速检索利用^[Di Vesta, F. J., & Gray, G. S. (1972). Listening and note taking. _Journal of Educational Psychology_, _63_(1), 8–14. [https://doi.org/10.1037/h0032243](https://doi.org/10.1037/h0032243)]。作为知识工作者，我们时刻需要知识来帮助我们解决问题——这既包括利用已有知识解决程序化问题，比如回忆起已知的办理步骤完成某个手续的办理；也包括利用已有知识推理出非程序化问题的解决方法，比如研究一个新的营销方案、就某个新问题写一篇论文。而在这个过程中，如何快速调用已有知识就成为了关键。这既可以通过增强已有知识的记忆来实现（比如利用 SuperMemo、Anki 等记忆软件），也可以通过利用外部载体记录已有知识、在需要时快速检索来实现。而后者，也就是“构建第二大脑”的根本目的，也是大家记录各种课堂笔记、论文笔记、工作笔记的根本原因。

## 2. 高效检索的方法

如何高效地检索已有知识呢？很多人的第一反应就是借助全文搜索。诚然，这个方法确实可以高效检索，但并非任何时候都能高效检索——全文搜索并不能解决多词一义的问题。比如，当我们全文检索“土豆”时，软件就会自动过滤包含“马铃薯”相关的内容。所以，我们还需要借助其他方法来解决这个问题。

本质上来看，信息的检索过程是通过检索符号来获得相关信息的过程。比如，当我们使用搜索引擎或全文检索时，我们所使用的关键词就是获得相关信息的检索符号。而检索符号的设计则会直接影响我们搜索的效率。举个例子，当我们因手头上的工作需要立马查找马铃薯相关内容时，我们直觉上会怎么做？我们第一反应肯定是去查找那些打了马铃薯标签的笔记，抑或查找那些在农作物/马铃薯分类下的笔记，但绝对不可能是想着某年某月某日我做了关于马铃薯的笔记。因此，检索符号的设计必须围绕着语义和信息主题出发。图书馆学家们很早就发现了这个问题，并发明了分类语言和主题语言来解决这个问题。

## 3. 向着自动推理进军

基于图书馆学家们发明的分类语言和主题语言，我们就能真正实现一个个人定制的、能够高效检索已有知识的笔记系统。这个笔记系统就好比做菜时有一个井井有条的冰箱，我们想做什么菜，就能快速地从中找到所需食材。

但目前为止，这个笔记系统只是起着存储素材的作用，能不能让这个笔记系统更智能一点，自动挖掘一下隐藏在素材中的潜在洞见呢？

这就不得不提知识图谱的应用了。根据知识图谱，我们可以轻松的发现实体之间的潜在联系。比如，已知 B 是 A 的朋友，D 是 B 的朋友，E 是 D 的朋友，我们则可以推得 A 和 D 也可能会相互认识。我们是不是能把这种逻辑应用于我们的笔记系统里呢？

![Pasted image 20221006142436](附件/Pasted%20image%2020221006142436.png)

说干就干，我又进一步研究了知识图谱相关内容。结果，我发现如果想实现上述的推理，首先要对知识进行符号化表示。而这与上一节说的主题语言不谋而合。因此，基于标题语言与知识图谱思想的 KG 笔记法就此诞生。（本库不对方法进行进一步说明，有兴趣的读者移步[这里](https://forum-zh.obsidian.md/t/topic/2059)。）

![Pasted image 20221007203325.gif](附件/Pasted%20image%2020221007203325.gif)

# 二、KG 笔记法

## 1. 概念准备

在 KG 笔记法中，一切信息都可以被分成三类：

- 综合讨论某个概念或实体的信息
- 讨论概念或实体某一方面的信息
- 讨论概念或实体与其他概念、实体间联系的信息

并且，基于知识图谱的理论，我们的笔记类型可以分成三种：

- 概念笔记：用于记录与某个概念相关的信息。比如，与马铃薯相关的信息记录在《马铃薯》中。
- 实体笔记：用于记录与某个实体相关的信息。比如，与Amazon.com（亚马逊）相关的信息记录在《Amazon.com》中。
- 关系笔记：记录实体、概念间关系相关的信息。比如关于马铃薯与红薯之间差别的信息记录在《马铃薯-对比-红薯》中。

无论哪种类型的笔记，笔记均通过标题来反应其内容。但由于关系笔记的内容比较复杂，用单一的标题名称无法很好地揭示笔记内容。因此，根据信息组织的主题语言^[张燕飞. (2005). _信息组织的主题语言_. 武汉：武汉大学出版社. ]，把关系笔记的名称又分成四小种：

- 关系：记录 A 与 B 之间的关系。比如，运动与健康之间的关系可以记于《运动-关系-健康》。
- 对比：记录 A 与 B 之间的比较、差异。比如，马铃薯与红薯之间的差异可以记于《马铃薯-对比-红薯》。
- 影响：记录 A 对 B 的影响。比如老师对学生的影响可以记于《老师-影响-学生》。
- 应用：记录 A 在 B 上的应用。比如，数学如何应用于管理可以记于《数学-应用-管理》。

这里需要注意以下三点：

1. 上面所说的 A 和 B 既可以是概念或实体，也可以是概念或实体间的关系。
2. 关系笔记也可以涉及多个对象，比如《A-B-C-对比》则代表“A、B、C之间的对比”。
3. 如何选择这四种关系笔记完全取决于你。对于相同的信息，可能有的人会觉得它是“对比”而有的人会觉得它只是在阐述“关系”，这都没关系，自己确定适合的类型就好。

## 2. 使用步骤

### 1. 将信息放入笔记中

在了解了上述概念以后，接下来我们要做的就是根据以下规则将所需记录的信息放入对应的笔记中：

- 对于那些综合讨论某个概念或实体的信息，我们将其放入对应的概念笔记或实体笔记中。
- 对于那些讨论某个概念或实体某一方面的信息，我们也将其放入对应的概念或实体笔记中，并在该笔记中创建相应的章节。需要注意的是，对于某个概念或实体某一方面的讨论，其自身也可能是一个独立的概念或实体。比如，虽然“汽车维修”虽然是“汽车”的某一方面，但其也可以视为一个独立的概念，因此我们可以将其记于独立的概念笔记中。
- 对于那些讨论概念或实体间关系的信息，我们将其放入对应的关系笔记中， 并在相应的概念或实体笔记中链接该关系笔记，即 `[[A]] -> [[A-关系-B]] <- [[B]]`。当然，很多时候 A 和 B 之间的关系可能是非常简单的，比如 `A 的爸爸是 B`。在这种情况下，我们没有必要为这个关系专门创建一篇关系笔记，而是使用链接即可。比如，在《A》中记录如下：`A 的爸爸是 [[B]]`。

此处需要注意的是一点是，如果我们记录的信息有出处的，我们需要及时标注出处，以方便未来溯源。这里推荐使用 Pandoc 的引用语法来标注出处，这样我们不仅可以溯源，还可以使用 Pandoc 一键生成符合格式的论文。

### 2. 收尾

在将信息放入对应笔记中后，我们还有几步需要完成：

1. 检查潜在关系。有些时候，笔记中会有一些潜在的或遗漏的关系。因此，我们需要重新检查一下笔记中是否还有未处理的潜在关系。如果我们发现了简单的关系，我们就直接链接相应的概念或实体笔记即可。比如我们在笔记《A》中发现 `A 的妈妈是 C` 这么一句话，我们只需要直接使用双链链接对应的实体笔记《C》，即 `A 的妈妈是 [[C]]`。如果我们发现了复杂的关系，则需要创建相应的关系笔记，然后将这些内容放入该关系笔记中。
2. 分离独立概念。正如前文所述，当我们在某篇笔记的某个章节下积累了越来越多的内容、对这个方面越来越了解之后，我们可能会发现这个章节实际可能对应着一个独立的概念或实体，或者我们可以私自地认为它是一个独立的概念或实体。因此，我们可以把这部分内容独立出来，在精简原有笔记的同时也方便内容搜索。比如，这篇文章中所述的方法应该是《笔记方法》的一章，但我也可以称其为“KG 笔记法”，将其视为一个新的独立的概念。
3. 分类与归档。最后，我们需要使用一种分类法将所做笔记分类归档。我们之所以要做这一步，一方面是防止某一文件夹内文件数量过多而导致系统卡顿，另一方面则是给信息检索提供一个新的渠道——分类检索。但这步也只是建议而非必须。在分类法方面，中图法、杜威十进制分类法、PARA，任何分类法都是可以的。选择哪种分类法取决于你自己的喜好与笔记量。

下图以动画方式大致展现了 KG 笔记法的整个过程。

![使用步骤](附件/使用步骤.gif)

## 3. 注意事项

### 1. “信息”的具体含义

前文中所讨论的“信息”，即可以指我们从书籍、论文、视频等任何信息源中做出的摘录与总结，也可以是我们独有的想法。从这个角度来说，KG 笔记法是一种信息或知识的组织方法，侧重于如何组织信息、知识，而非告诉你应该去记录哪些信息。（我认为所谓组织方法，就应该侧重于如何组织，而不是告诉你哪些该记哪些不该记。）

### 2. 命名的问题

另外，概念笔记和实体笔记的命名是相对随意的，因为命名的根本目的是赋予笔记内信息一个独立的检索标识。因此，只要我们知道这个检索标识会返回哪些信息，无论我们是使用普遍接受的名称作为检索标识，还是使用自己随意取的名称作为检索标识，都无关紧要。

但是，命名时我们需要注意多词同义和一词多义的问题。如果这两个问题不解决，则会降低我们的搜索效率。

所谓多词同义是指相同的内容可以使用不同的名称来作为检索标识。比如关于马铃薯的信息，我们既可以将它存放到《马铃薯》里，也可以将它存放到《土豆》里。这会使相同主题的信息散落在不同的检索标识中。当我们检索时无法穷尽所有的检索标识，我们就无法检索到所需的全部内容。这会降低我们检索的效率。（这也是关键词全文搜索的问题所在。）

所谓一词多义是指不同的内容可以使用同一名称来作为检索标识。比如在哲学中、HTML中、知识图谱中都有“属性”这一概念。我们既可能会将关于哲学中“属性”的内容放入《属性》内，也可能将 HTML 中关于属性的说明放入《属性》内。这就会使得我们检索时返回过多无关内容，降低检索效率。（这也是关键词全文搜索的问题所在。）

那么如何解决这两个问题呢？信息组织的主题语言也早已准备了解决方案。对于多词同义的问题，我们需要将不同的检索标识同时与同一段信息相关联。比如，对于讲述马铃薯的信息，我们可以同时赋予其“土豆”和“马铃薯”的标识。而对于一词多义的问题，我们可以通过修饰语来进一步的明晰检索标识。比如哲学中的“属性”使用 `属性（哲学）` 表示，HMTL 中的属性使用 `属性（HTML）` 表示。当然，带修饰语的检索标识并不符合我们搜索的直觉，因此我们可以将不带修饰语的符号将其关联，这样我们就既能使用符合直觉的符号，也能精准的区分不同领域的信息。具体实践方法见[下文](#2.%20高效检索)。

# 三、功能示意

综上，KG 笔记法具有知识融合、高效检索和简单推理三个特点，接下来本库将对这三个用法进行进一步说明。

## 1. 知识融合

知识融合是高效检索的前提，也是个人知识管理系统和图书馆最大的区别。毕竟讲述同一个主题的书可以由不同的作者出版成百上千本，但对于个人来说，一个主题的知识就应当汇聚在一起，方便我们后期利用时一次性检索完全。由于 KG 笔记法以严格控制的标题为检索符号，因此我们在记录新知识时能很方便地将同一个主题的知识内容记录到同一篇笔记上，从而把相同主题的知识融合在一起。

比如，无论是现在还是未来，当我看了关于“父母心理控制”的文章，想摘抄原文或产生了新想法新洞见时，我都能轻松地找到《父母心理控制》这篇笔记，将摘录或灵感登记于其上，方便我后续检索利用。

![Pasted image 20221007193220.png](附件/Pasted%20image%2020221007193220.png)

## 2. 高效检索

与侧重于搜索的方法不同，KG 法将工作重心前移到了组织环节，将严格控制的标题作为检索符号，以降低后期检索的复杂性。

比如，当我想要进一步查找“父母心理控制”相关内容时，我只需要在 Obsidian 的快速切换中输入“父母心理控制”即可定位到相关笔记，并在该笔记中通过小标题进一步定位所需信息。而当我想查找“父母心理控制和外化问题行为之间的关系的时候”，我只要输入“父母心理控制-关系-外化问题行为”即可定位到相关笔记。（你们也可以试试）

![Pasted image 20221006143631.gif](附件/Pasted%20image%2020221006143631.gif)

当然，很多时候一个概念不会只有一个名称。而根据前文所述的叙词语言的词形控制和词义控制思想，KG 法利用 Obsidian 的别名来解决概念的多名称问题。比如查找父母心理控制相关内容，我也可以使用“psychological control”这一英文概念名称。

![Pasted image 20221006145129.gif](附件/Pasted%20image%2020221006145129.gif)

而不同概念需要使用同个名称的时候，KG 法就会使用带修饰语的标题来区分相同的标题，并且利用别名来方便搜索。比如，关于哲学中“属性”的内容，会记录在《属性（哲学）》中，并且赋予其 `哲学` 的别名。这样无论直接搜索标题 `哲学（属性）` 还是 `哲学`，都能找到这段信息。

![](附件/Pasted%20image%2020221105230837.gif)

最后，如果我重读了笔记中的内容但仍然无法理解时，我可以通过笔记末尾的 pandoc 引用语法 `[@citekey, page]`，使用 [Quicker动作](https://getquicker.net/Sharedaction?code=d76ca089-0769-4a61-8a63-08d916bcf619) 快速跳转回原文献 PDF，从而结合上下文进一步回忆理解笔记内容。

![Pasted image 20221006145916.gif](附件/Pasted%20image%2020221006145916.gif)

## 3. 知识推理

KG 法的另一特征就是将标题作为语义化的检索符号，结合知识图谱的思想，从而能一定程度上基于笔记内容对潜在关系进行推理。

比如，当我需要写一篇关于“父母控制是否会导致孩子焦虑”的论文时，我可以通过 Path-finder 插件检索以《父母控制》这篇笔记为起点、以《焦虑》这篇笔记为终点的路径图。

![Pasted image 20221006150351.gif](附件/Pasted%20image%2020221006150351.gif)

如结果所示， Path-finder 插件为我绘制了十余条可能的路径。

![Pasted image 20221006102437.png](附件/Pasted%20image%2020221006102437.png)

接下来我需要做的，只需要判断哪条路径在逻辑上最为可行即可。并且，由于 KG 法知识融合的特性，每篇笔记都汇聚了所有关于其标题的内容，因此我不必再打开文献库查找原始文献，而只需要打开路径上的笔记即可对路径进行深入研究。

![Pasted image 20221006150723.png](附件/Pasted%20image%2020221006150723.png)

# 四、场景示例：应用 KG 法于写作

在 KG 法的帮助下，使用笔记输出文章就变得比较具有实际操作性了：

1. 可以在大脑中或 Obsidain 中随意漫游节点，想想看哪两个节点可能存在关联。
2. 使用 Path-finder 来计算这两个节点间的潜在逻辑路径。
3. 在计算结果中找到我们觉得逻辑上最为可行的那条路径。
4. 阅读路径上经过的笔记，进一步研究这条路径是否切实可行。
5. 将路径代表的逻辑转换为文章。文章所需要使用的引文可从笔记中直接获取，一般无需重新翻阅文献库。
6. 利用 Pandoc 排版，并自动生成参考文献，
7. 发表/发布文章。

# 五、尾声

示例到这里就结束了。其实将 Obsidian 用于知识管理和知识输出并不是门槛极高的事，并不需要我们把插件商店的六百多个插件研究透彻，关键在于我们是否真的去记录和管理了我们的知识。

根据以往学员的反馈，本方法平均练习记录几十篇笔记后即可上手。如果在使用中遇到了疑惑，或是想将方法应用到自己所从事的领域，欢迎通过 [Obsidian 中文论坛](https://forum-zh.obsidian.md/u/ryooo/summary)、[知乎](https://www.zhihu.com/people/rao-yao-47-68)或 [邮箱](kgnotes@163.com) 联系我，我会和你一同探索。

P.S. 最近建了个微信群，有兴趣的朋友可以私信我加入。