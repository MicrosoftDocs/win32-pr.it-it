---
title: Codifica Two-Pass
description: Codifica Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, codifica a due passaggi
- Windows Media Format SDK, codifica a 2 passaggi
- codec, codifica a due passaggi
- codec, codifica a 2 passaggi
- codifica a due passaggi, informazioni
- codifica a 2 passaggi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044474"
---
# <a name="two-pass-encoding"></a><span data-ttu-id="7fead-109">Codifica Two-Pass</span><span class="sxs-lookup"><span data-stu-id="7fead-109">Two-Pass Encoding</span></span>

<span data-ttu-id="7fead-110">La codifica a due passaggi è un metodo di codifica disponibile con alcuni codec, ad esempio il codec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="7fead-110">Two-pass encoding is an encoding method available with some codecs, like the Windows Media Video 9 codec.</span></span> <span data-ttu-id="7fead-111">Quando si usa la codifica a due passaggi, il codec elabora due volte tutti gli esempi per il flusso.</span><span class="sxs-lookup"><span data-stu-id="7fead-111">When you use two-pass encoding, the codec processes all of the samples for the stream twice.</span></span> <span data-ttu-id="7fead-112">Al primo passaggio, il codec raccoglie informazioni sul contenuto del flusso.</span><span class="sxs-lookup"><span data-stu-id="7fead-112">On the first pass, the codec gathers information about the content of the stream.</span></span> <span data-ttu-id="7fead-113">Al secondo passaggio, il codec usa le informazioni raccolte al primo passaggio per ottimizzare il processo di codifica per il flusso.</span><span class="sxs-lookup"><span data-stu-id="7fead-113">On the second pass, the codec uses the information gathered on the first pass to optimize the encoding process for the stream.</span></span>

<span data-ttu-id="7fead-114">Nella modalità di codifica della velocità in bit costante i file codificati in due passaggi sono in genere più efficienti rispetto ai file codificati in un singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="7fead-114">In the Constant Bit Rate encoding mode, files that are encoded in two passes are generally more efficient than files encoded in a single pass.</span></span> <span data-ttu-id="7fead-115">Il VBR basato sulla qualità, che è un passaggio, produce una qualità più uniforme rispetto a quella basata sulla velocità in bit, ovvero due passaggi.</span><span class="sxs-lookup"><span data-stu-id="7fead-115">Quality-based VBR, which is one pass, produces more consistent quality than bit-rate-based VBR, which is two-pass.</span></span>

<span data-ttu-id="7fead-116">Non è possibile usare la codifica a due passaggi sui flussi live.</span><span class="sxs-lookup"><span data-stu-id="7fead-116">You cannot use two-pass encoding on live streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fead-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fead-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fead-118">**Funzionalità di codec**</span><span class="sxs-lookup"><span data-stu-id="7fead-118">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="7fead-119">**Uso della codifica Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="7fead-119">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




