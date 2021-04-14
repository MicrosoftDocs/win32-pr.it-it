---
title: Librerie e intestazioni obbligatorie per un provider di servizi
description: Librerie e intestazioni obbligatorie per un provider di servizi
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Media Gestione dispositivi, librerie
- Gestione dispositivi, librerie
- Guida per programmatori, librerie
- provider di servizi, librerie
- creazione di provider di servizi, librerie
- libraries
- Windows Media Gestione dispositivi, file di intestazione
- Gestione dispositivi, file di intestazione
- Guida per programmatori, file di intestazione
- provider di servizi, file di intestazione
- creazione di provider di servizi, file di intestazione
- file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b987d389216a3349c6797517b48c03bbb4d0f1eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330372"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Librerie e intestazioni obbligatorie per un provider di servizi

In questa sezione sono elencate le librerie, i file di intestazione o i file IDL che è necessario includere per sviluppare un'applicazione Windows Media Gestione dispositivi o un plug-in. Come indicato nella pagina relativa alla [compilazione dei file IDL forniti con l'SDK](compiling-the-idl-files-supplied-with-the-sdk.md), l'SDK include sia i file IDL che i file di intestazione predefiniti, che possono essere usati dall'applicazione. Si noti che alcuni file di intestazione non hanno file IDL corrispondenti e non è possibile compilarli manualmente. Se si compilano file IDL personalizzati, includere le dipendenze elencate nella compilazione dei file IDL forniti con l'SDK.

Non tutte le applicazioni richiedono tutti i file; leggere la descrizione per sapere se l'applicazione richiede un file.



| Intestazione o libreria predefinita       | IDL equivalente                                                                | Descrizione                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | Nessuno                                                                          | Richiesto da tutti i provider di servizi. Definisce oggetti Windows Media Gestione dispositivi.                                                                                                                                                                               |
| Initguid. h                       | None (intestazione Platform SDK)                                                    | Richiesto da tutti i provider di servizi per definire i valori **GUID** utilizzando il file mswmdm. h predefinito. È necessario includere Initguid. h una sola volta nel progetto. Questa intestazione ridefinisce la macro **\_ GUID define** per evitare problemi di denominazione dei **GUID** esterni. |
| mswmdm. h                         | WMDM. idl<br/> WMSP. idl<br/> IComponentAuthenticate. idl<br/> | Richiesto da tutti i provider di servizi. Definisce tutte le interfacce, le strutture, i metadati, i codici di errore e altre costanti del provider di servizi.                                                                                                                        |
| SAC. h                            | Nessuno                                                                          | Richiesto da tutti i provider di servizi. Definisce i protocolli SAC.                                                                                                                                                                                                      |
| scserver. h                       | Nessuno                                                                          | Richiesto da tutti i provider di servizi. Dichiara la classe [CSecureChannelServer](csecurechannelserver-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                                                   | Obbligatorio per i provider di servizi che usano l'interfaccia [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| WMSDK. h                          | Nessuno (fornito da Windows Media Format SDK)                                   | Obbligatorio per i provider di servizi che usano i metodi Windows Media Format SDK.                                                                                                                                                                                      |
| wmvcore. lib                      | Nessuno                                                                          | Obbligatorio per i provider di servizi che utilizzano oggetti o funzioni di Windows Media Format SDK.                                                                                                                                                                          |
| mmreg. h                          | None (intestazione Platform SDK)                                                    | Obbligatorio per i provider di servizi che fanno riferimento a varie definizioni di formato Windows Media standard, ad esempio **WAVEFORMATEX**.                                                                                                                                      |
| MtpExt. h                         | Nessuno                                                                          | Obbligatorio per i provider di servizi che gestiscono [**IMDSPDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) nei dispositivi MTP. Definisce varie costanti e strutture MTP standard.                                                                        |
| Chiave. c                            | Nessuno                                                                          | Definisce una chiave e un certificato da Microsoft. La versione fornita con l'SDK include una chiave fittizia di test che consentirà l'uso di file Windows Media non protetti da DRM.                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 





