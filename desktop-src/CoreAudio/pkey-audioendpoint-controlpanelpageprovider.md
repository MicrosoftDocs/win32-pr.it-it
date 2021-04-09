---
description: La \_ Proprietà pkey AudioEndpoint \_ ControlPanelPageProvider specifica il CLSID del provider registrato dell'estensione delle proprietà del dispositivo per il dispositivo dell'endpoint audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877797"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a><span data-ttu-id="42dd2-103">PKEY \_ AudioEndpoint \_ ControlPanelPageProvider</span><span class="sxs-lookup"><span data-stu-id="42dd2-103">PKEY\_AudioEndpoint\_ControlPanelPageProvider</span></span>

<span data-ttu-id="42dd2-104">La proprietà **pkey \_ AudioEndpoint \_ CONTROLPANELPAGEPROVIDER** specifica il CLSID del provider registrato dell'estensione delle proprietà del dispositivo per il dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="42dd2-104">The **PKEY\_AudioEndpoint\_ControlPanelPageProvider** property specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span> <span data-ttu-id="42dd2-105">L'estensione fornisce le proprietà dell'endpoint audio visualizzate nella pagina dispositivo-proprietà del pannello di controllo multimediale di Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="42dd2-105">The extension supplies the audio endpoint properties that are displayed in the device-properties page of the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="42dd2-106">Per ulteriori informazioni su Mmsys.cpl, vedere la documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="42dd2-106">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="42dd2-107">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="42dd2-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="42dd2-108">Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null contenente un GUID che identifica il provider dell'estensione del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="42dd2-108">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the provider of the control-panel extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="42dd2-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42dd2-109">Requirements</span></span>



| <span data-ttu-id="42dd2-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="42dd2-110">Requirement</span></span> | <span data-ttu-id="42dd2-111">Valore</span><span class="sxs-lookup"><span data-stu-id="42dd2-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42dd2-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42dd2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="42dd2-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42dd2-113">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="42dd2-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42dd2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="42dd2-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42dd2-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="42dd2-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42dd2-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="42dd2-117"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="42dd2-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42dd2-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42dd2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42dd2-119">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="42dd2-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="42dd2-120">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="42dd2-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




