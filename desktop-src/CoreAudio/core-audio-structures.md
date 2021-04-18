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
# <a name="core-audio-structures"></a>Strutture audio di base

In questa sezione vengono descritte le strutture utilizzate dalle API audio principali in Windows Vista e versioni successive.



| Struttura                                                                     | Descrizione                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_dati di \_ notifica \_ volume audio**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Descrive una modifica a livello di volume o di muting di un dispositivo endpoint audio.                                                                                 |
| [**\_parametri di \_ attivazione \_ audio DirectX**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Specifica i parametri di inizializzazione per un flusso DirectSound.                                                                                                   |
| [**Descrizione di KSJACK \_**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Recuperato tramite [**IKsJackDescription:: GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); descrive un jack audio.                                 |
| [**\_DESCRIPTION2 KSJACK**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Recuperato tramite [**IKsJackDescription2:: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); descrive un jack audio. <br/>                 |
| [**\_ \_ informazioni sul sink KSJACK**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Recuperato tramite [**IKsJackSinkInformation:: GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); descrive un sink di Jack audio.<br/> |
| [**LUID**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Archivia l'identificatore della porta video.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

 




