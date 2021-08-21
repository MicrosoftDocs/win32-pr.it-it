---
description: Strutture audio di base
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Strutture audio di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8ea83d0de4c07c1a3d36bab169d5cb581e82cf60e84e308d04dff49af0dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407215"
---
# <a name="core-audio-structures"></a>Strutture audio di base

Questa sezione descrive le strutture usate dalle API audio di base in Windows Vista e versioni successive.



| Struttura                                                                     | Descrizione                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATI DI \_ NOTIFICA VOLUME \_ \_ AUDIO**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Descrive una modifica del livello del volume o dello stato di muto di un dispositivo endpoint audio.                                                                                 |
| [**PARAMETRI DI \_ ATTIVAZIONE AUDIO \_ \_ DIRECTX**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Specifica i parametri di inizializzazione per un flusso DirectSound.                                                                                                   |
| [**DESCRIZIONE DI \_ KSJACK**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Recuperato tramite [**IKsDescription::GetDescriptionDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); descrive un jack audio.                                 |
| [**KSJACK \_ DESCRIPTION2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Recuperato tramite [**IKsDescription2::GetDescriptionDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); descrive un jack audio. <br/>                 |
| [**INFORMAZIONI SUL SINK KSJACK \_ \_**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Recuperato tramite [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); descrive un sink jack audio.<br/> |
| [**Luid**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Archivia l'identificatore di porta video.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> </dl>

 

 




