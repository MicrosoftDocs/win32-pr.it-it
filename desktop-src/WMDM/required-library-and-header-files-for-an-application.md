---
title: Libreria e file di intestazione necessari per un'applicazione
description: Libreria e file di intestazione necessari per un'applicazione
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Gestione dispositivi multimediali, librerie
- Gestione dispositivi, librerie
- guida per programmatori,librerie
- applicazioni desktop, librerie
- creazione Windows applicazioni,librerie di Gestione dispositivi multimediali
- libraries
- Windows Gestione dispositivi multimediali, file di intestazione
- Gestione dispositivi, file di intestazione
- guida per programmatori,file di intestazione
- applicazioni desktop, file di intestazione
- creazione Windows applicazioni gestione dispositivi multimediali,file di intestazione
- file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b6630f4ff752b53ed69633d1e63a62093e4a4fbd16f65ccb1cc709aae120a07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863071"
---
# <a name="required-library-and-header-files-for-an-application"></a>Libreria e file di intestazione necessari per un'applicazione

Questa sezione elenca le librerie, i file di intestazione o i file IDL che è necessario includere per sviluppare un'applicazione o un plug-in di Gestione dispositivi multimediali Windows. Come accennato in Compilazione dei file IDL forniti con [l'SDK, l'SDK](compiling-the-idl-files-supplied-with-the-sdk.md)include sia i file IDL che i file di intestazione predefiniti e l'applicazione può usare entrambi. Si noti che alcuni file di intestazione non hanno file IDL corrispondenti e non è possibile compilarli manualmente. Se si compilano file IDL personalizzati, includere le dipendenze elencate in Compilazione dei file IDL forniti con l'SDK.

Non tutte le applicazioni richiedono tutti i file. Leggere la descrizione per sapere se l'applicazione richiede un file.



| Intestazione o libreria predefinite       | IDL equivalente                                | Descrizione                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp.lib                     | Nessuno                                          | Obbligatorio per tutte le applicazioni. Contiene Windows oggetti di Gestione dispositivi multimediali.                                                                                                                                                                              |
| wmvcore.lib                      | Nessuno                                          | Obbligatorio per le applicazioni che usano Windows oggetti o funzioni di Media Format SDK.                                                                                                                                                                          |
| initguid.h                       | none (intestazione di Platform SDK)                    | Obbligatorio per tutte le applicazioni per definire **i valori GUID** usando il file Mswmdm.h predefinito. È necessario includere initguid.h una sola volta nel progetto. Questa intestazione ridefinisce la macro **DEFINE \_ GUID** per evitare problemi di denominazione **dei GUID** esterni. |
| mmreg.h                          | none (intestazione di Platform SDK)                    | Obbligatorio per le applicazioni che fanno riferimento a Windows di formato multimediale standard, ad esempio **WAVEFORMATEX**.                                                                                                                                      |
| mswmdm.h                         | WMDM.idlicomponentauthenticate.idl<br/> | Obbligatorio per tutte le applicazioni. Definisce tutte le interfacce dell'applicazione, nonché strutture, metadati, errori e altre costanti.                                                                                                                        |
| sac.h                            | Nessuno                                          | Obbligatorio per tutte le applicazioni. Definisce i protocolli SAC.                                                                                                                                                                                                      |
| scclient.h                       | Nessuno                                          | Obbligatorio per tutte le applicazioni. Dichiara la [classe CSecureChannelClient.](csecurechannelclient-class.md)                                                                                                                                                  |
| wmdmlog.hwmdmlog \_ i.c<br/> | Wmdmlog.idl                                   | Richiesto dalle applicazioni che usano [**l'interfaccia IWMDMLogger.**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)                                                                                                                                                                       |
| wmdrmdeviceapp.h                 | WMDRMDeviceApp.idl                            | Richiesto dalle applicazioni o dai plug-in che aggiornano i componenti DRM o il contatore play conta sui dispositivi.                                                                                                                                                          |
| wmsdk.h                          | none (fornito da Windows Media Format SDK)   | Obbligatorio per le applicazioni che usano Windows Media Format SDK.                                                                                                                                                                                      |
| MtpExt.h                         | Nessuno                                          | Obbligatorio per le applicazioni che chiamano [**IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) nei dispositivi MTP. Definisce varie costanti e strutture MTP standard.                                                                          |
| Key.c                            | Nessuno                                          | Definisce una chiave e un certificato da Microsoft. La versione fornita con l'SDK include una chiave fittizia di test che consentirà l'uso di file multimediali non protetti da DRM Windows multimediali.                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 





