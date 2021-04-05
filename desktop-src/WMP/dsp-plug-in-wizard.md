---
title: Procedura guidata plug-in DSP
description: Procedura guidata plug-in DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Plug-in di Windows Media Player, creazione guidata plug-in
- plug-in, creazione guidata plug-in
- plug-in di elaborazione dei segnali digitali, creazione guidata plug-in
- Plug-in DSP, creazione guidata plug-in
- procedura guidata plug-in
- Visual Studio, creazione guidata plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515694"
---
# <a name="dsp-plug-in-wizard"></a><span data-ttu-id="cc9b8-109">Procedura guidata plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="cc9b8-109">DSP Plug-in Wizard</span></span>

<span data-ttu-id="cc9b8-110">Windows Media Player SDK fornisce una procedura guidata plug-in che è possibile aggiungere a Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cc9b8-110">The Windows Media Player SDK provides a plug-in wizard that you can add to Visual Studio.</span></span> <span data-ttu-id="cc9b8-111">La procedura guidata può generare codice di esempio per un'ampia gamma di plug-in, inclusi i seguenti tipi di plug-in DSP:</span><span class="sxs-lookup"><span data-stu-id="cc9b8-111">The wizard can generate sample code for a variety of plug-ins, including the following types of DSP plug-ins:</span></span>

-   <span data-ttu-id="cc9b8-112">Plug-in DSP audio</span><span class="sxs-lookup"><span data-stu-id="cc9b8-112">Audio DSP plug-in</span></span>
-   <span data-ttu-id="cc9b8-113">Plug-in DSP audio (modalità duale)</span><span class="sxs-lookup"><span data-stu-id="cc9b8-113">Audio DSP plug-in (dual mode)</span></span>
-   <span data-ttu-id="cc9b8-114">Plug-in DSP video</span><span class="sxs-lookup"><span data-stu-id="cc9b8-114">Video DSP plug-in</span></span>
-   <span data-ttu-id="cc9b8-115">Plug-in video DSP (modalità duale)</span><span class="sxs-lookup"><span data-stu-id="cc9b8-115">Video DSP plug-in (dual mode)</span></span>

<span data-ttu-id="cc9b8-116">Ognuno dei due plug-in di esempio di base, DSP audio e video DSP, funziona come un oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="cc9b8-116">Each of the two basic sample plug-ins, Audio DSP and Video DSP, functions as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="cc9b8-117">Ovvero ogni plug-in di esempio implementa l'interfaccia **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="cc9b8-117">That is, each sample plug-in implements the **IMediaObject** interface.</span></span> <span data-ttu-id="cc9b8-118">Ognuno dei due plug-in di esempio dual mode può fungere da DMO o come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="cc9b8-118">Each of the two dual-mode sample plug-ins can function either as a DMO or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="cc9b8-119">Ovvero, ogni plug-in di esempio Dual-Mode implementa sia l'interfaccia **IMediaObject** che l'interfaccia **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="cc9b8-119">That is, each dual-mode sample plug-in implements both the **IMediaObject** interface and the **IMFTransform** interface.</span></span>

<span data-ttu-id="cc9b8-120">È possibile compilare, collegare, registrare e testare il codice del plug-in di esempio.</span><span class="sxs-lookup"><span data-stu-id="cc9b8-120">You can compile, link, register, and test the sample plug-in code.</span></span> <span data-ttu-id="cc9b8-121">È quindi possibile modificare il codice di esempio generato per creare il plug-in DSP personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cc9b8-121">Then you can modify the generated sample code to create your own DSP plug-in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc9b8-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc9b8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc9b8-123">**Creazione di un plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="cc9b8-123">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> <dt>

[<span data-ttu-id="cc9b8-124">**Panoramica per gli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="cc9b8-124">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="cc9b8-125">**Aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11**</span><span class="sxs-lookup"><span data-stu-id="cc9b8-125">**Updates to the DSP Plug-in Wizard for Windows Media Player 11**</span></span>](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




