---
title: Librerie e intestazioni necessarie per un provider di servizi
description: Librerie e intestazioni necessarie per un provider di servizi
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Gestione dispositivi multimediali, librerie
- Gestione dispositivi, librerie
- guida per programmatori,librerie
- provider di servizi, librerie
- creazione di provider di servizi, librerie
- libraries
- Windows Gestione dispositivi multimediali, file di intestazione
- Gestione dispositivi, file di intestazione
- guida per programmatori, file di intestazione
- provider di servizi, file di intestazione
- creazione di provider di servizi, file di intestazione
- file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72628d2f8582e7d729e27d7745ff1716c376d475afcaa48e52099f6cf63d2d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903931"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Librerie e intestazioni necessarie per un provider di servizi

Questa sezione elenca le librerie, i file di intestazione o i file IDL che è necessario includere per sviluppare un'applicazione o un plug-in di Gestione dispositivi di Windows. Come accennato in Compilazione dei file IDL forniti con [l'SDK](compiling-the-idl-files-supplied-with-the-sdk.md), l'SDK include sia i file IDL che i file di intestazione predefiniti e l'applicazione può usare entrambi. Si noti che alcuni file di intestazione non hanno file IDL corrispondenti e non è possibile compilarli manualmente. Se si compilano file IDL personalizzati, includere le dipendenze elencate in Compilazione dei file IDL forniti con l'SDK.

Non tutte le applicazioni richiedono tutti i file. Leggere la descrizione per sapere se l'applicazione richiede un file.



| Intestazione o libreria precompilata       | IDL equivalente                                                                | Descrizione                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp.lib                     | Nessuno                                                                          | Obbligatorio per tutti i provider di servizi. Definisce Windows oggetti di Gestione dispositivi multimediali.                                                                                                                                                                               |
| initguid.h                       | none (intestazione Platform SDK)                                                    | Richiesto da tutti i provider di servizi per definire **i valori GUID** usando il file Mswmdm.h predefinito. È necessario includere initguid.h una sola volta nel progetto. Questa intestazione ridefinisce la macro **DEFINE \_ GUID** per evitare problemi di denominazione **dei GUID** esterni. |
| mswmdm.h                         | WMDM.idl<br/> WMSP.idl<br/> icomponentauthenticate.idl<br/> | Obbligatorio per tutti i provider di servizi. Definisce tutte le interfacce, le strutture, i metadati, i codici di errore e altre costanti del provider di servizi.                                                                                                                        |
| sac.h                            | Nessuno                                                                          | Obbligatorio per tutti i provider di servizi. Definisce i protocolli SAC.                                                                                                                                                                                                      |
| scserver.h                       | Nessuno                                                                          | Obbligatorio per tutti i provider di servizi. Dichiara la [classe CSecureChannelServer.](csecurechannelserver-class.md)                                                                                                                                                  |
| wmdmlog.hwmdmlog \_ i.c<br/> | Wmdmlog.idl                                                                   | Richiesto dai provider di servizi che usano [**l'interfaccia IWMDMLogger.**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)                                                                                                                                                                       |
| wmsdk.h                          | none (fornito da Windows Media Format SDK)                                   | Obbligatorio per i provider di servizi che usano Windows media format SDK.                                                                                                                                                                                      |
| wmvcore.lib                      | Nessuno                                                                          | Richiesto dai provider di servizi che usano Windows oggetti o funzioni di Media Format SDK.                                                                                                                                                                          |
| mmreg.h                          | none (intestazione Platform SDK)                                                    | Richiesto dai provider di servizi che fanno riferimento a varie definizioni di Windows standard, ad esempio **WAVEFORMATEX.**                                                                                                                                      |
| MtpExt.h                         | Nessuno                                                                          | Obbligatorio per i provider di servizi [**che gestiscono IMDSPDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) nei dispositivi MTP. Definisce varie costanti e strutture MTP standard.                                                                        |
| Key.c                            | Nessuno                                                                          | Definisce una chiave e un certificato di Microsoft. La versione fornita con l'SDK include una chiave fittizia di test che consentirà l'uso di file multimediali non protetti Windows DRM.                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 





