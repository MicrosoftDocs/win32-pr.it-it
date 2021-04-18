---
description: Strutture audio di base
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Strutture audio di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304428"
---
# <a name="core-audio-structures"></a><span data-ttu-id="e3698-103">Strutture audio di base</span><span class="sxs-lookup"><span data-stu-id="e3698-103">Core Audio Structures</span></span>

<span data-ttu-id="e3698-104">In questa sezione vengono descritte le strutture utilizzate dalle API audio principali in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e3698-104">This section describes the structures that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="e3698-105">Struttura</span><span class="sxs-lookup"><span data-stu-id="e3698-105">Structure</span></span>                                                                     | <span data-ttu-id="e3698-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3698-106">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3698-107">**\_dati di \_ notifica \_ volume audio**</span><span class="sxs-lookup"><span data-stu-id="e3698-107">**AUDIO\_VOLUME\_NOTIFICATION\_DATA**</span></span>](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | <span data-ttu-id="e3698-108">Descrive una modifica a livello di volume o di muting di un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="e3698-108">Describes a change in the volume level or muting state of an audio endpoint device.</span></span>                                                                                 |
| [<span data-ttu-id="e3698-109">**\_parametri di \_ attivazione \_ audio DirectX**</span><span class="sxs-lookup"><span data-stu-id="e3698-109">**DIRECTX\_AUDIO\_ACTIVATION\_PARAMS**</span></span>](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | <span data-ttu-id="e3698-110">Specifica i parametri di inizializzazione per un flusso DirectSound.</span><span class="sxs-lookup"><span data-stu-id="e3698-110">Specifies the initialization parameters for a DirectSound stream.</span></span>                                                                                                   |
| [<span data-ttu-id="e3698-111">**Descrizione di KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="e3698-111">**KSJACK\_DESCRIPTION**</span></span>](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | <span data-ttu-id="e3698-112">Recuperato tramite [**IKsJackDescription:: GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); descrive un jack audio.</span><span class="sxs-lookup"><span data-stu-id="e3698-112">Retrieved through [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describes an audio jack.</span></span>                                 |
| [<span data-ttu-id="e3698-113">**\_DESCRIPTION2 KSJACK**</span><span class="sxs-lookup"><span data-stu-id="e3698-113">**KSJACK\_DESCRIPTION2**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | <span data-ttu-id="e3698-114">Recuperato tramite [**IKsJackDescription2:: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); descrive un jack audio.</span><span class="sxs-lookup"><span data-stu-id="e3698-114">Retrieved through [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describes an audio jack.</span></span> <br/>                 |
| [<span data-ttu-id="e3698-115">**\_ \_ informazioni sul sink KSJACK**</span><span class="sxs-lookup"><span data-stu-id="e3698-115">**KSJACK\_SINK\_INFORMATION**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | <span data-ttu-id="e3698-116">Recuperato tramite [**IKsJackSinkInformation:: GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); descrive un sink di Jack audio.</span><span class="sxs-lookup"><span data-stu-id="e3698-116">Retrieved through [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describes an audio jack sink.</span></span><br/> |
| [<span data-ttu-id="e3698-117">**LUID**</span><span class="sxs-lookup"><span data-stu-id="e3698-117">**LUID**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | <span data-ttu-id="e3698-118">Archivia l'identificatore della porta video.</span><span class="sxs-lookup"><span data-stu-id="e3698-118">Stores the video port identifier.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="e3698-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3698-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3698-120">Guida di riferimento alla programmazione</span><span class="sxs-lookup"><span data-stu-id="e3698-120">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




