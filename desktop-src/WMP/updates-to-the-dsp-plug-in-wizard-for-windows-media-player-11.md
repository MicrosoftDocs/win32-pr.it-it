---
title: Aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11
description: Aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Plug-in di Windows Media Player, creazione guidata plug-in
- plug-in, creazione guidata plug-in
- plug-in di elaborazione dei segnali digitali, creazione guidata plug-in
- Plug-in DSP, creazione guidata plug-in
- procedura guidata plug-in
- Visual Studio, creazione guidata plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398583"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a><span data-ttu-id="8809e-109">Aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="8809e-109">Updates to the DSP Plug-in Wizard for Windows Media Player 11</span></span>

<span data-ttu-id="8809e-110">Windows Media Player 11 SDK introduce le seguenti modifiche alla procedura guidata plug-in di DSP:</span><span class="sxs-lookup"><span data-stu-id="8809e-110">The Windows Media Player 11 SDK introduces the following changes to the DSP plug-in wizard:</span></span>

-   <span data-ttu-id="8809e-111">I plug-in registrano il modello di threading come "both".</span><span class="sxs-lookup"><span data-stu-id="8809e-111">Plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="8809e-112">Questo consente l'esecuzione del plug-in nella pipeline Media Foundation in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8809e-112">This enables the plug-in to run in the Media Foundation pipeline on Windows Vista.</span></span> <span data-ttu-id="8809e-113">Vedere il file *NomeProgetto*. RGS.</span><span class="sxs-lookup"><span data-stu-id="8809e-113">See the *projectname*.rgs file.</span></span>

    -   <span data-ttu-id="8809e-114">I plug-in audio DSP hanno il supporto per i due formati aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8809e-114">Audio DSP plug-ins have support for the following two additional formats:</span></span>

    <!-- -->

    -   <span data-ttu-id="8809e-115">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="8809e-115">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
    -   <span data-ttu-id="8809e-116">\_Formato Wave \_ estendibile con subformat KSDATAFORMAT \_ sottotipo \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="8809e-116">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

    <span data-ttu-id="8809e-117">Vedere il file *NomeProgetto*. cpp.</span><span class="sxs-lookup"><span data-stu-id="8809e-117">See the *projectname*.cpp file.</span></span>

    1.  <span data-ttu-id="8809e-118">I plug-in video DSP hanno il supporto per il formato video NV12.</span><span class="sxs-lookup"><span data-stu-id="8809e-118">Video DSP plug-ins have support for the NV12 video format.</span></span>
    2.  <span data-ttu-id="8809e-119">I plug-in effettuano chiamate aggiuntive a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuovo tipo di plug-in: WMP \_ plug- \_ DSP \_ OUTOFPROC.</span><span class="sxs-lookup"><span data-stu-id="8809e-119">Plug-ins make additional calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC.</span></span> <span data-ttu-id="8809e-120">Vedere il file *projectnamedll*. cpp del progetto.</span><span class="sxs-lookup"><span data-stu-id="8809e-120">See the project's *projectnamedll*.cpp file.</span></span>
    3.  <span data-ttu-id="8809e-121">Un progetto aggiuntivo in ogni soluzione crea una DLL proxy/stub per l'interfaccia personalizzata delle impostazioni della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8809e-121">An additional project in each solution creates a proxy/stub DLL for the property page settings custom interface.</span></span> <span data-ttu-id="8809e-122">Vedere il progetto *projectnamePS* .</span><span class="sxs-lookup"><span data-stu-id="8809e-122">See the *projectnamePS* project.</span></span>
    4.  <span data-ttu-id="8809e-123">Le chiamate ai metodi deprecati sono state modificate in modo da usare le versioni più recenti.</span><span class="sxs-lookup"><span data-stu-id="8809e-123">Calls to deprecated methods have been changed to use the newest versions.</span></span>
    5.  <span data-ttu-id="8809e-124">La procedura guidata può generare un plug-in dual mode che funziona sia come DMO, implementando **IMediaObject** e come MFT, implementando **IMFTransform**.</span><span class="sxs-lookup"><span data-stu-id="8809e-124">The wizard can generate a dual-mode plug-in that functions both as a DMO, by implementing **IMediaObject**, and as an MFT, by implementing **IMFTransform**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8809e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8809e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8809e-126">**Procedura guidata plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="8809e-126">**DSP Plug-in Wizard**</span></span>](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




