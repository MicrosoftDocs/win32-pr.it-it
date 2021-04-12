---
title: Interfacce plug-in DSP
description: Interfacce plug-in DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Plug-in di Windows Media Player, interfacce DSP
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce DSP
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- plug-in per l'elaborazione di segnali digitali, interfaccia ISpecifyPropertyPage
- Plug-in DSP, interfacce
- Plug-in DSP, interfaccia ISpecifyPropertyPage
- interfacce, plug-in DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104398744"
---
# <a name="dsp-plug-in-interfaces"></a><span data-ttu-id="db23a-113">Interfacce plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="db23a-113">DSP Plug-in Interfaces</span></span>

<span data-ttu-id="db23a-114">Le interfacce del plug-in DSP (Digital Signal Processing) vengono utilizzate per gestire il trasferimento dei dati tra Windows Media Player e il plug-in.</span><span class="sxs-lookup"><span data-stu-id="db23a-114">The digital signal processing (DSP) plug-in interfaces are used to manage data transfer between Windows Media Player and the plug-in.</span></span> <span data-ttu-id="db23a-115">Tutti i plug-in DSP possono implementare facoltativamente l'interfaccia **ISpecifyPropertyPage** per fornire un'implementazione della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="db23a-115">All DSP plug-ins may optionally implement the **ISpecifyPropertyPage** interface to provide a property page implementation.</span></span>

<span data-ttu-id="db23a-116">Per la creazione di plug-in DSP sono necessarie le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="db23a-116">The following interfaces are required for creating DSP plug-ins.</span></span>



| <span data-ttu-id="db23a-117">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="db23a-117">Interface</span></span>                                                | <span data-ttu-id="db23a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db23a-118">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db23a-119">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="db23a-119">**IMediaObject**</span></span>                                         | <span data-ttu-id="db23a-120">Gestisce lo scambio di dati con Windows Media Player ed esegue attività di elaborazione di segnali digitali.</span><span class="sxs-lookup"><span data-stu-id="db23a-120">Manages data exchange with Windows Media Player and performs digital signal processing tasks.</span></span> <span data-ttu-id="db23a-121">La documentazione dettagliata è inclusa in DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="db23a-121">Detailed documentation is included with the DirectX SDK.</span></span> |
| [<span data-ttu-id="db23a-122">IWMPMediaPluginRegistrar</span><span class="sxs-lookup"><span data-stu-id="db23a-122">IWMPMediaPluginRegistrar</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | <span data-ttu-id="db23a-123">Gestisce la registrazione del plug-in.</span><span class="sxs-lookup"><span data-stu-id="db23a-123">Manages plug-in registration.</span></span>                                                                                                                          |
| [<span data-ttu-id="db23a-124">IWMPPlugin</span><span class="sxs-lookup"><span data-stu-id="db23a-124">IWMPPlugin</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | <span data-ttu-id="db23a-125">Gestisce la connessione a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="db23a-125">Manages the connection to Windows Media Player.</span></span>                                                                                                        |
| [<span data-ttu-id="db23a-126">IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="db23a-126">IWMPPluginEnable</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | <span data-ttu-id="db23a-127">Archivia se il plug-in è attualmente abilitato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="db23a-127">Stores whether the plug-in is currently enabled by Windows Media Player.</span></span>                                                                               |
| [<span data-ttu-id="db23a-128">IWMPServices</span><span class="sxs-lookup"><span data-stu-id="db23a-128">IWMPServices</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | <span data-ttu-id="db23a-129">Recupera le informazioni dal lettore sull'ora del flusso corrente e sullo stato del flusso.</span><span class="sxs-lookup"><span data-stu-id="db23a-129">Retrieves information from the Player about the current stream time and stream state.</span></span>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="db23a-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db23a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db23a-131">**Guida di riferimento alla programmazione di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="db23a-131">**DSP Plug-ins Programming Reference**</span></span>](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




