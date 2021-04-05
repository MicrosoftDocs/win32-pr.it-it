---
title: Informazioni su IWMPPluginEnable
description: Informazioni su IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
- Plug-in di Windows Media Player, interfaccia IWMPPluginEnable
- plug-in, interfaccia IWMPPluginEnable
- plug-in per l'elaborazione di segnali digitali, interfaccia IWMPPluginEnable
- Plug-in DSP, interfaccia IWMPPluginEnable
- Interfaccia IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955195"
---
# <a name="about-iwmppluginenable"></a><span data-ttu-id="01a05-113">Informazioni su IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="01a05-113">About IWMPPluginEnable</span></span>

<span data-ttu-id="01a05-114">L'interfaccia **IWMPPluginEnable** è necessaria per i plug-in di Windows Media Player DSP. **IWMPPluginEnable** contiene due metodi che archiviano se Windows Media Player ha abilitato il plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="01a05-114">The **IWMPPluginEnable** interface is required for Windows Media Player DSP plug-ins. **IWMPPluginEnable** contains two methods that store whether Windows Media Player has enabled the DSP plug-in.</span></span> <span data-ttu-id="01a05-115">Windows Media Player chiama **IWMPPluginEnable:: seenable** quando crea un'istanza del plug-in DSP, passando un valore **true** se il plug-in è stato abilitato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01a05-115">Windows Media Player calls **IWMPPluginEnable::SetEnable** when it creates an instance of the DSP plug-in, passing a value of **TRUE** if it has enabled the plug-in or **FALSE** otherwise.</span></span>

<span data-ttu-id="01a05-116">È possibile che i plug-in DSP rimangano caricati anche quando l'utente sceglie di disabilitarli.</span><span class="sxs-lookup"><span data-stu-id="01a05-116">DSP plug-ins may remain loaded even when the user chooses to disable them.</span></span> <span data-ttu-id="01a05-117">Quando è disabilitato, un plug-in deve copiare i dati dal buffer di input nel buffer di output, eseguendo solo l'elaborazione della conversione del formato, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="01a05-117">When disabled, a plug-in must copy data from the input buffer to the output buffer, performing only format conversion processing, if applicable.</span></span>

<span data-ttu-id="01a05-118">Windows Media Player chiama inoltre questo metodo prima di rilasciare un'istanza del plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="01a05-118">Windows Media Player also calls this method before it releases an instance of the DSP plug-in.</span></span> <span data-ttu-id="01a05-119">Questa operazione è utile per consentire ai client del plug-in di verificare se il plug-in è attualmente abilitato.</span><span class="sxs-lookup"><span data-stu-id="01a05-119">This is useful to allow clients of the plug-in to check whether the plug-in is currently enabled.</span></span> <span data-ttu-id="01a05-120">Un plug-in dell'interfaccia utente, ad esempio, potrebbe modificare l'aspetto dei controlli per avvisare l'utente che il plug-in DSP non è connesso.</span><span class="sxs-lookup"><span data-stu-id="01a05-120">For instance, a user interface plug-in might change the appearance of its controls to alert the user that the DSP plug-in is not connected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01a05-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01a05-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a05-122">**Interfacce obbligatorie**</span><span class="sxs-lookup"><span data-stu-id="01a05-122">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




