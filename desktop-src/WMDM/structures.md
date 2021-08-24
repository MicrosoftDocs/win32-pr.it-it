---
title: Strutture WMDM
description: Questo articolo include articoli di riferimento sulle strutture definite da Windows Media Device Manager, ad esempio _BITMAPINFOHEADER e MTP_COMMAND_DATA_IN.
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Windows Gestione dispositivi multimediali, strutture
- Gestione dispositivi, strutture
- informazioni di riferimento sulla programmazione, strutture
- informazioni di riferimento Windows Gestione dispositivi multimediali, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd0048a7cf3b87f09bb46ef6f6db74531b4b67a7364acd28099feed04bb8dec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865541"
---
# <a name="wmdm-structures"></a>Strutture WMDM

Windows Gestione dispositivi multimediali definisce le strutture seguenti.



| Struttura                                                   | Descrizione                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Definisce il formato del fotogramma video.                                                                                                                                                                                                                       |
| [**DATI DEL COMANDO MTP \_ \_ \_ IN**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Contiene i comandi personalizzati MTP (Media Transport Protocol) inviati al dispositivo usando il metodo [**IWMDMDevice3::D eviceIoControl.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol)                                                                           |
| [**DATI DEL COMANDO MTP \_ \_ \_ OUT**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Contiene le risposte MTP (Media Transport Protocol) compilate dal driver di dispositivo.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | Contiene i dati per i comandi passati Windows Gestione dispositivi multimediali a un dispositivo, ma che non devono essere utilizzati da Windows Gestione dispositivi multimediali.                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | Definisce il formato di un flusso video.                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | Definisce il formato dei dati waveform-audio.                                                                                                                                                                                                               |
| [**FUNZIONALITÀ DEL \_ FORMATO WMDM \_**](wmdm-format-capability.md)  | Descrive le funzionalità di un dispositivo per un formato specifico. Questa struttura contiene un set di configurazioni di proprietà in una matrice di [**strutture \_ PROP \_ CONFIG WMDM.**](wmdm-prop-config.md)                                                       |
| [**WMDM \_ PROP \_ CONFIG**](wmdm-prop-config.md)              | Descrive un set di valori di proprietà compatibili tra tutte le proprietà supportate dal dispositivo per un formato specifico. Questa struttura contiene una serie di descrizioni di proprietà in una matrice di [**strutture \_ PROP \_ DESC WMDM.**](wmdm-prop-desc.md) |
| [**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)                  | Descrive i valori validi di una proprietà in una particolare configurazione di proprietà.                                                                                                                                                                             |
| [**ENUMERAZIONE DEI VALORI DELLA PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-enum.md)   | Contiene un set enumerato di valori validi per una determinata proprietà in una particolare configurazione di proprietà.                                                                                                                                             |
| [**INTERVALLO DI VALORI DELLA PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-range.md) | Descrive l'intervallo di valori validi per una determinata proprietà in una particolare configurazione di proprietà.                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | Contiene una data e un'ora.                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | Descrive i numeri di serie e gli ID gruppo.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Definisce la visualizzazione dei metadati.                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | Descrive i diritti di utilizzo del contenuto.                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | Descrive un tipo MIME.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




