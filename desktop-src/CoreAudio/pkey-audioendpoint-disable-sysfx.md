---
description: La \_ Proprietà pkey AudioEndpoint \_ Disable \_ SysFx specifica se gli effetti di sistema sono abilitati nel flusso in modalità condivisa che scorre verso o dal dispositivo dell'endpoint audio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127310"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a><span data-ttu-id="a0a13-103">PKEY \_ AudioEndpoint \_ Disabilita \_ SysFx</span><span class="sxs-lookup"><span data-stu-id="a0a13-103">PKEY\_AudioEndpoint\_Disable\_SysFx</span></span>

<span data-ttu-id="a0a13-104">La proprietà **pkey \_ AudioEndpoint \_ Disable \_ SysFx** specifica se gli effetti di sistema sono abilitati nel flusso in modalità condivisa che scorre verso o dal dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="a0a13-104">The **PKEY\_AudioEndpoint\_Disable\_SysFx** property specifies whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>

<span data-ttu-id="a0a13-105">Gli effetti di sistema sono implementati come oggetti di elaborazione audio (APOs) che possono essere inseriti in un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="a0a13-105">System effects are implemented as audio processing objects (APOs) that can be inserted into an audio stream.</span></span> <span data-ttu-id="a0a13-106">APOs sono moduli software che eseguono funzioni di elaborazione audio quali il controllo del volume e la conversione del formato.</span><span class="sxs-lookup"><span data-stu-id="a0a13-106">APOs are software modules that perform audio processing functions such as volume control and format conversion.</span></span> <span data-ttu-id="a0a13-107">La disabilitazione degli effetti di sistema per un dispositivo endpoint consente al flusso associato di passare attraverso il APOs non modificato.</span><span class="sxs-lookup"><span data-stu-id="a0a13-107">Disabling the system effects for an endpoint device enables the associated stream to pass through the APOs unmodified.</span></span>

<span data-ttu-id="a0a13-108">Per ulteriori informazioni sugli effetti di sistema in Windows Vista, vedere i white paper intitolati "effettivi audio personalizzati in Windows Vista" e "riutilizzo di Windows Vista Audio System Effects" nel sito Web [tecnologie per dispositivi audio per Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="a0a13-108">For more information about system effects in Windows Vista, see the white papers titled "Custom Audio Effects in Windows Vista" and "Reusing Windows Vista Audio System Effects" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="a0a13-109">Questa proprietà si applica solo agli effetti locali e agli effetti globali APOs installati dal file con estensione inf che ha installato la scheda audio a cui è connesso il dispositivo endpoint.</span><span class="sxs-lookup"><span data-stu-id="a0a13-109">This property applies only to the local-effects and global-effects APOs that were installed by the .inf file that installed the audio adapter to which the endpoint device is connected.</span></span> <span data-ttu-id="a0a13-110">Inoltre, questa proprietà influisce solo sul dispositivo endpoint di destinazione, ma non ha alcun effetto sugli effetti del sistema per altri dispositivi endpoint, anche se si connettono alla stessa scheda.</span><span class="sxs-lookup"><span data-stu-id="a0a13-110">In addition, this property affects only the target endpoint device—it has no effect on the system effects for any other endpoint devices, even if they connect to the same adapter.</span></span>

<span data-ttu-id="a0a13-111">Il membro **VT** della struttura **PROPVARIANT** è impostato su **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="a0a13-111">The **vt** member of the **PROPVARIANT** structure is set to **VT\_UI4**.</span></span>

<span data-ttu-id="a0a13-112">Il membro **ulVal** della struttura **PROPVARIANT** è impostato su **endpoint \_ SYSFX \_ Enabled** se gli effetti di sistema sono abilitati o sull' **endpoint \_ SYSFX \_ disabilitato** se sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="a0a13-112">The **ulVal** member of the **PROPVARIANT** structure is set to **ENDPOINT\_SYSFX\_ENABLED** if system effects are enabled or to **ENDPOINT\_SYSFX\_DISABLED** if they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a13-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0a13-113">Requirements</span></span>



| <span data-ttu-id="a0a13-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0a13-114">Requirement</span></span> | <span data-ttu-id="a0a13-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a0a13-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a13-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0a13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a13-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0a13-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a0a13-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0a13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a13-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0a13-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a0a13-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0a13-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0a13-121"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0a13-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a13-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0a13-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a13-123">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="a0a13-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="a0a13-124">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="a0a13-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




