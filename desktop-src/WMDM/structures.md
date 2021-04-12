---
title: Strutture WMDM
description: Strutture
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Windows Media Gestione dispositivi, strutture
- Gestione dispositivi, strutture
- riferimento alla programmazione, strutture
- informazioni di riferimento su Windows Media Gestione dispositivi, sulle strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903aa07bbe3d01029eb2020b521523b545843f2a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104398328"
---
# <a name="wmdm-structures"></a>Strutture WMDM

Windows Media Gestione dispositivi definisce le strutture seguenti.



| Struttura                                                   | Descrizione                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Definisce il formato del fotogramma video.                                                                                                                                                                                                                       |
| [**\_ \_ dati del comando MTP \_ in**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Contiene i comandi personalizzati MTP (Media Transport Protocol) che vengono inviati al dispositivo usando il metodo [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) .                                                                           |
| [**dati del comando MTP in \_ \_ \_ uscita**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Contiene le risposte MTP (Media Transport Protocol) compilate dal driver di dispositivo.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | Contiene i dati per i comandi passati attraverso Windows Media Gestione dispositivi a un dispositivo ma che non devono essere utilizzati da Windows Media Gestione dispositivi.                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | Definisce il formato di un flusso video.                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | Definisce il formato dei dati audio della forma d'onda.                                                                                                                                                                                                               |
| [**\_funzionalità di formato WMDM \_**](wmdm-format-capability.md)  | Descrive le funzionalità di un dispositivo per un particolare formato. Questa struttura contiene un set di configurazioni di proprietà in una matrice di strutture [**WMDM \_ prop \_ config**](wmdm-prop-config.md) .                                                       |
| [**\_configurazione della prop WMDM \_**](wmdm-prop-config.md)              | Descrive un set di valori di proprietà compatibili tra tutte le proprietà supportate dal dispositivo per un particolare formato. Questa struttura contiene un numero di descrizioni delle proprietà in una matrice di strutture [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) . |
| [**WMDM \_ prop \_ DESC**](wmdm-prop-desc.md)                  | Descrive i valori validi di una proprietà in una configurazione di proprietà specifica.                                                                                                                                                                             |
| [**\_ \_ enumerazione valori Prop \_ WMDM**](wmdm-prop-values-enum.md)   | Contiene un set enumerato di valori validi per una particolare proprietà in una particolare configurazione della proprietà.                                                                                                                                             |
| [**WMDM \_ \_ intervallo valori \_ prop**](wmdm-prop-values-range.md) | Descrive l'intervallo di valori validi per una particolare proprietà in una particolare configurazione della proprietà.                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | Contiene una data e un'ora.                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | Vengono descritti i numeri di serie e gli ID di gruppo.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Definisce la visualizzazione dei metadati.                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | Descrive i diritti di utilizzo del contenuto.                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | Descrive un tipo MIME.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




