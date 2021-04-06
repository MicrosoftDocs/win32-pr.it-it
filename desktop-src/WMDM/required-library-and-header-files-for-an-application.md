---
title: File di intestazione e di libreria necessari per un'applicazione
description: File di intestazione e di libreria necessari per un'applicazione
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Media Gestione dispositivi, librerie
- Gestione dispositivi, librerie
- Guida per programmatori, librerie
- applicazioni desktop, librerie
- creazione di applicazioni Windows Media Gestione dispositivi, librerie
- libraries
- Windows Media Gestione dispositivi, file di intestazione
- Gestione dispositivi, file di intestazione
- Guida per programmatori, file di intestazione
- applicazioni desktop, file di intestazione
- creazione di applicazioni Windows Media Gestione dispositivi, file di intestazione
- file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a8a04ee6c3fe603d52139e83f81a49d78dc45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044843"
---
# <a name="required-library-and-header-files-for-an-application"></a>File di intestazione e di libreria necessari per un'applicazione

In questa sezione sono elencate le librerie, i file di intestazione o i file IDL che è necessario includere per sviluppare un'applicazione Windows Media Gestione dispositivi o un plug-in. Come indicato nella pagina relativa alla [compilazione dei file IDL forniti con l'SDK](compiling-the-idl-files-supplied-with-the-sdk.md), l'SDK include sia i file IDL che i file di intestazione predefiniti, che possono essere usati dall'applicazione. Si noti che alcuni file di intestazione non hanno file IDL corrispondenti e non è possibile compilarli manualmente. Se si compilano file IDL personalizzati, includere le dipendenze elencate nella compilazione dei file IDL forniti con l'SDK.

Non tutte le applicazioni richiedono tutti i file; leggere la descrizione per sapere se l'applicazione richiede un file.



| Intestazione o libreria predefinita       | IDL equivalente                                | Descrizione                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | Nessuno                                          | Richiesto da tutte le applicazioni. Contiene oggetti Windows Media Gestione dispositivi.                                                                                                                                                                              |
| wmvcore. lib                      | Nessuno                                          | Richiesto dalle applicazioni che utilizzano oggetti o funzioni di Windows Media Format SDK.                                                                                                                                                                          |
| Initguid. h                       | None (intestazione Platform SDK)                    | Richiesto da tutte le applicazioni per definire i valori **GUID** utilizzando il file mswmdm. h predefinito. È necessario includere Initguid. h una sola volta nel progetto. Questa intestazione ridefinisce la macro **\_ GUID define** per evitare problemi di denominazione dei **GUID** esterni. |
| mmreg. h                          | None (intestazione Platform SDK)                    | Richiesto dalle applicazioni che fanno riferimento a varie definizioni di formato Windows Media standard, ad esempio **WAVEFORMATEX**.                                                                                                                                      |
| mswmdm. h                         | WMDM. idlicomponentauthenticate. idl<br/> | Richiesto da tutte le applicazioni. Definisce tutte le interfacce dell'applicazione, nonché le strutture, i metadati, gli errori e altre costanti.                                                                                                                        |
| SAC. h                            | Nessuno                                          | Richiesto da tutte le applicazioni. Definisce i protocolli SAC.                                                                                                                                                                                                      |
| scclient. h                       | Nessuno                                          | Richiesto da tutte le applicazioni. Dichiara la classe [CSecureChannelClient](csecurechannelclient-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                   | Richiesto dalle applicazioni che utilizzano l'interfaccia [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| wmdrmdeviceapp. h                 | WMDRMDeviceApp. idl                            | Richiesto dalle applicazioni o dai plug-in che aggiornano i componenti di DRM o i conteggi delle giocazioni dei contatori nei dispositivi.                                                                                                                                                          |
| WMSDK. h                          | Nessuno (fornito da Windows Media Format SDK)   | Obbligatorio per le applicazioni che usano i metodi Windows Media Format SDK.                                                                                                                                                                                      |
| MtpExt. h                         | Nessuno                                          | Obbligatorio per le applicazioni che chiamano [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) nei dispositivi MTP. Definisce varie costanti e strutture MTP standard.                                                                          |
| Chiave. c                            | Nessuno                                          | Definisce una chiave e un certificato da Microsoft. La versione fornita con l'SDK include una chiave fittizia di test che consentirà l'uso di file Windows Media non protetti da DRM.                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 





