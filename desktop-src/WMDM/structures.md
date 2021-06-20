---
title: Strutture WMDM
description: Questo articolo include articoli di riferimento sulle strutture definite da Gestione dispositivi di Windows Media, ad esempio _BITMAPINFOHEADER e MTP_COMMAND_DATA_IN.
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Gestione dispositivi di Windows Media, strutture
- Gestione dispositivi, strutture
- informazioni di riferimento sulla programmazione, strutture
- informazioni di riferimento per Gestione dispositivi di Windows Media, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc49deb3f4dd28695f5e0e7c3a871c53fa96300
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406504"
---
# <a name="wmdm-structures"></a>Strutture WMDM

Gestione dispositivi di Windows Media definisce le strutture seguenti.



| Struttura                                                   | Descrizione                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Definisce il formato del fotogramma video.                                                                                                                                                                                                                       |
| [**DATI DEL COMANDO MTP \_ \_ \_ IN**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Contiene i comandi personalizzati MTP (Media Transport Protocol) inviati al dispositivo usando il metodo [**IWMDMDevice3::D eviceIoControl.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol)                                                                           |
| [**MTP \_ COMMAND \_ DATA \_ OUT**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Contiene le risposte MTP (Media Transport Protocol) compilate dal driver di dispositivo.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | Contiene i dati per i comandi che vengono passati tramite Gestione dispositivi multimediali di Windows a un dispositivo, ma che non devono essere utilizzati da Gestione dispositivi multimediali di Windows.                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | Definisce il formato di un flusso video.                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | Definisce il formato dei dati audio della forma d'onda.                                                                                                                                                                                                               |
| [**FUNZIONALITÀ DEL FORMATO \_ \_ WMDM**](wmdm-format-capability.md)  | Descrive le funzionalità di un dispositivo per un particolare formato. Questa struttura contiene un set di configurazioni di proprietà in una matrice di [**strutture \_ PROP \_ CONFIG WMDM.**](wmdm-prop-config.md)                                                       |
| [**WMDM \_ PROP \_ CONFIG**](wmdm-prop-config.md)              | Descrive un set di valori di proprietà compatibili in tutte le proprietà supportate dal dispositivo per un particolare formato. Questa struttura contiene una serie di descrizioni di proprietà in una matrice di [**strutture \_ DESC PROP \_ WMDM.**](wmdm-prop-desc.md) |
| [**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)                  | Descrive i valori validi di una proprietà in una particolare configurazione di proprietà.                                                                                                                                                                             |
| [**ENUMERAZIONE DEI VALORI DELLE PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-enum.md)   | Contiene un set enumerato di valori validi per una determinata proprietà in una particolare configurazione di proprietà.                                                                                                                                             |
| [**INTERVALLO DI VALORI DELLE PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-range.md) | Descrive l'intervallo di valori validi per una determinata proprietà in una particolare configurazione di proprietà.                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | Contiene una data e un'ora.                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | Descrive i numeri di serie e gli ID gruppo.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Definisce la visualizzazione dei metadati.                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | Descrive i diritti di utilizzo del contenuto.                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | Descrive un tipo MIME.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




