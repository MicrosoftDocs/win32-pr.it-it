---
title: Enumerazione dei sink
description: Enumerazione dei sink
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- ASF (Advanced Systems Format), enumerazione di sink
- ASF (formato avanzato dei sistemi), enumerazione di sink
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724029"
---
# <a name="enumerating-sinks"></a><span data-ttu-id="8cc3b-108">Enumerazione dei sink</span><span class="sxs-lookup"><span data-stu-id="8cc3b-108">Enumerating Sinks</span></span>

<span data-ttu-id="8cc3b-109">Il writer può avere molti sink associati.</span><span class="sxs-lookup"><span data-stu-id="8cc3b-109">The writer can have many sinks associated with it.</span></span> <span data-ttu-id="8cc3b-110">È possibile enumerare i sink aggiunti al writer usando [**IWMWriterAdvanced:: GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) e [**IWMWriterAdvanced:: getsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span><span class="sxs-lookup"><span data-stu-id="8cc3b-110">You can enumerate the sinks that have been added to the writer by using [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) and [**IWMWriterAdvanced::GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span></span>

<span data-ttu-id="8cc3b-111">Il codice di esempio presente nei [messaggi di errore ottenuti da un sink](getting-error-messages-from-a-sink.md) illustra l'enumerazione sink.</span><span class="sxs-lookup"><span data-stu-id="8cc3b-111">The example code in the [Getting Error Messages from a Sink](getting-error-messages-from-a-sink.md) demonstrates sink enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="8cc3b-112">Quando si enumerano i sink, il sink di file predefinito creato in risposta a una chiamata a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) verrà enumerato insieme a tutti gli altri sink aggiunti.</span><span class="sxs-lookup"><span data-stu-id="8cc3b-112">When enumerating sinks, the default file sink created in response to a call to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) will be enumerated along with any other sinks you have added.</span></span> <span data-ttu-id="8cc3b-113">Se si usa solo il sink di file predefinito, è possibile accedervi chiamando **getsink** per l'indice di sink 0.</span><span class="sxs-lookup"><span data-stu-id="8cc3b-113">If you are using only the default file sink, you can access it by calling **GetSink** for sink index 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8cc3b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cc3b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cc3b-115">**Interfaccia IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="8cc3b-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="8cc3b-116">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="8cc3b-116">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




