---
title: Elementi inclusi nell'SDK
description: Elementi inclusi nell'SDK
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows Gestione dispositivi multimediali, Software Development Kit (SDK)
- Gestione dispositivi, Software Development Kit (SDK)
- Windows Sdk di Gestione dispositivi multimediali
- SDK di Gestione dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36e621ac4de7fee296bf9d2c3ffb4e1d357824510b37a6ded73efd66b91f38d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004901"
---
# <a name="whats-included-with-the-sdk"></a>Elementi inclusi nell'SDK

La tabella seguente descrive il contenuto dell'SDK Windows Media Device Manager. Tutti i file o le cartelle sono descritti in relazione al percorso di installazione radice dell'SDK.



| File                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Cartella di primo livello per l'SDK Windows Media Device Manager. Questa cartella include il makefile per la compilazione di tutte le applicazioni di esempio.                                                                                                                                                                                                                                                                                                              |
| Idl\\                      | Cartella che contiene tutti i file IDL necessari per compilare le intestazioni necessarie Windows metodi di Gestione dispositivi multimediali. Tuttavia, invece di usare questi file, è possibile usare i file di intestazione forniti nella cartella \\ inc.<br/> Per visualizzare un elenco di questi file IDL e per informazioni sui file di intestazione compilati dai file IDL, vedere Compilazione dei file IDL forniti [con l'SDK](compiling-the-idl-files-supplied-with-the-sdk.md).<br/> |
| inc \\ ....<br/>       | Cartella che include tutte le intestazioni che definiscono le interfacce e i tipi di dati in questo SDK.                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm.h                   | Definisce tutte le interfacce dell'applicazione, le interfacce del provider di servizi, le interfacce del provider di contenuti protette, i codici di errore, le costanti, le strutture e [**l'interfaccia IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)                                                                                                                                                                                                                            |
| mswmdm \_ i.c                | Definisce [**l'interfaccia IWMDMNotification.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt.h                   | Definisce le strutture specifiche di MTP necessarie per le applicazioni che chiamano [**IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol).                                                                                                                                                                                                                                                                                                            |
| resource.h                 | Definisce varie costanti di risorsa usate dagli esempi di SDK.                                                                                                                                                                                                                                                                                                                                                                                         |
| sac.h                      | Definisce i dati del canale autenticato protetti richiesti da tutte le applicazioni e i provider di servizi.                                                                                                                                                                                                                                                                                                                                                       |
| scclient.h                 | Definisce la [classe CSecureChannelClient](csecurechannelclient-class.md) richiesta da tutte le applicazioni.                                                                                                                                                                                                                                                                                                                                              |
| scserver.h                 | Definisce la classe [CSecureChannelServer](csecurechannelserver-class.md) richiesta da tutti i provider di servizi.                                                                                                                                                                                                                                                                                                                                         |
| wmdm \_ ver.h                | Informazioni sulla versione facoltative Windows Gestione dispositivi multimediali.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog.h, wmdmlog \_ i.c    | Obbligatorio per le applicazioni o i provider di servizi che usano [**l'interfaccia IWMDMLogger.**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp.h           | Obbligatorio per le applicazioni che gestiscono la misurazione del contenuto (vedere [Controllo dell'utilizzo del contenuto).](metering-content-usage.md)                                                                                                                                                                                                                                                                                                                                  |
| wmsstd.h                   | Definisce le macro helper usate dagli esempi sdk.                                                                                                                                                                                                                                                                                                                                                                                                      |
| Lib\\                      | Cartella che contiene le librerie Windows Gestione dispositivi multimediali.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp.lib               | Libreria statica richiesta da tutti i Windows e dai provider di servizi di Gestione dispositivi multimediali.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto.lib              | La libreria statica richiesta da tutte Windows applicazioni di Gestione dispositivi multimediali e dai provider di servizi che usano DRM.                                                                                                                                                                                                                                                                                                                                    |
| mdsp \\ ....<br/>      | Cartella che contiene il codice per un provider di servizi di esempio. Per informazioni su questo esempio, incluso come compilarlo ed eseguirlo, vedere [Provider di servizi di esempio](sample-service-provider.md).                                                                                                                                                                                                                                                    |
| apps \\ ....<br/>      | Cartella che contiene due sottocartelle che contengono due metà del codice per un'applicazione desktop di esempio fornita con l'SDK. Per informazioni su questo esempio, incluso come compilarlo, vedere [Applicazione desktop di esempio](sample-desktop-application.md).                                                                                                                                                                                      |
| devicekit \\ ....<br/> | Cartella che contiene una suite di strumenti per testare il dispositivo portatile Windows Gestione dispositivi multimediali 11. I test includono l'enumerazione e il trasferimento di dispositivi e file, le funzionalità DRM e la conformità MTP. Questi strumenti hanno un proprio file di documentazione.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività iniziali**](getting-started.md)
</dt> </dl>

 

 





