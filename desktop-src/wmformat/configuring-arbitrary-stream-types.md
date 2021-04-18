---
title: Configurazione di tipi di flusso arbitrari
description: Configurazione di tipi di flusso arbitrari
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- flussi, configurazione di tipi di flusso arbitrari
- codec, configurazione di tipi di flusso arbitrari
- flussi, GenProfile
- codec, GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298215"
---
# <a name="configuring-arbitrary-stream-types"></a><span data-ttu-id="a888a-108">Configurazione di tipi di flusso arbitrari</span><span class="sxs-lookup"><span data-stu-id="a888a-108">Configuring Arbitrary Stream Types</span></span>

<span data-ttu-id="a888a-109">Per la maggior parte dei tipi di flusso arbitrario è sufficiente una velocità in bit, una finestra del buffer e un tipo di supporto principale appropriato nella struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="a888a-109">Most arbitrary stream types just need a bit rate, a buffer window, and a proper major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="a888a-110">Tuttavia, alcuni tipi arbitrari richiedono una configurazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="a888a-110">However, some arbitrary types require additional configuration.</span></span>

<span data-ttu-id="a888a-111">Se si riscontrano problemi durante la configurazione di un flusso, vedere l'applicazione di esempio denominata GenProfile, inclusa in questo SDK.</span><span class="sxs-lookup"><span data-stu-id="a888a-111">If you have trouble configuring a stream, refer to the sample application called GenProfile, which is included with this SDK.</span></span> <span data-ttu-id="a888a-112">La libreria definita in GenProfile contiene il codice per includere tutti i tipi di flussi.</span><span class="sxs-lookup"><span data-stu-id="a888a-112">The library defined in GenProfile contains code for including all types of streams.</span></span> <span data-ttu-id="a888a-113">Per ulteriori informazioni su GenProfile e sugli altri esempi, vedere [applicazioni di esempio](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a888a-113">For more information about GenProfile and the other samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="a888a-114">Nelle sezioni seguenti viene descritto come configurare i tipi di flusso arbitrari.</span><span class="sxs-lookup"><span data-stu-id="a888a-114">The following sections describe how to configure arbitrary stream types.</span></span>



| <span data-ttu-id="a888a-115">Sezione</span><span class="sxs-lookup"><span data-stu-id="a888a-115">Section</span></span>                                                                                                                                        | <span data-ttu-id="a888a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a888a-116">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a888a-117">Configurazione di flussi di script</span><span class="sxs-lookup"><span data-stu-id="a888a-117">Configuring Script Streams</span></span>](configuring-script-streams.md)                                                                                   | <span data-ttu-id="a888a-118">Viene descritto come configurare i flussi di script.</span><span class="sxs-lookup"><span data-stu-id="a888a-118">Describes how to configure script streams.</span></span>                                                  |
| [<span data-ttu-id="a888a-119">Configurazione di flussi di trasferimento di file</span><span class="sxs-lookup"><span data-stu-id="a888a-119">Configuring File Transfer Streams</span></span>](configuring-file-transfer-streams.md)                                                                     | <span data-ttu-id="a888a-120">Viene descritto come configurare i flussi di trasferimento di file.</span><span class="sxs-lookup"><span data-stu-id="a888a-120">Describes how to configure file transfer streams.</span></span>                                           |
| [<span data-ttu-id="a888a-121">Configurazione di flussi Web</span><span class="sxs-lookup"><span data-stu-id="a888a-121">Configuring Web Streams</span></span>](configuring-web-streams.md)                                                                                         | <span data-ttu-id="a888a-122">Viene descritto come configurare i flussi Web.</span><span class="sxs-lookup"><span data-stu-id="a888a-122">Describes how to configure Web streams.</span></span>                                                     |
| [<span data-ttu-id="a888a-123">Configurazione di flussi di testo</span><span class="sxs-lookup"><span data-stu-id="a888a-123">Configuring Text Streams</span></span>](configuring-text-streams.md)                                                                                       | <span data-ttu-id="a888a-124">Viene descritto come configurare i flussi di testo.</span><span class="sxs-lookup"><span data-stu-id="a888a-124">Describes how to configure text streams.</span></span>                                                    |
| [<span data-ttu-id="a888a-125">Configurazione di flussi arbitrari personalizzati</span><span class="sxs-lookup"><span data-stu-id="a888a-125">Configuring Custom Arbitrary Streams</span></span>](configuring-custom-arbitrary-streams.md)                                                               | <span data-ttu-id="a888a-126">Viene descritto come configurare i flussi per i tipi di flusso arbitrari personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a888a-126">Describes how to configure streams for custom arbitrary stream types.</span></span>                       |
| [<span data-ttu-id="a888a-127">Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari</span><span class="sxs-lookup"><span data-stu-id="a888a-127">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | <span data-ttu-id="a888a-128">Viene descritto come calcolare la velocità in bit e le impostazioni della finestra del buffer per un flusso arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a888a-128">Describes how to calculate the bit rate and buffer window settings for an arbitrary stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a888a-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a888a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a888a-130">**Flussi arbitrari**</span><span class="sxs-lookup"><span data-stu-id="a888a-130">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="a888a-131">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="a888a-131">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




