---
title: Contenuto dell'SDK
description: Contenuto dell'SDK
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows Media Gestione dispositivi, Software Development Kit (SDK)
- Gestione dispositivi, Software Development Kit (SDK)
- Windows Media Gestione dispositivi SDK
- SDK di Gestione dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac1698336e1cf3966e3ab69ad3ae7c46f95e469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044342"
---
# <a name="whats-included-with-the-sdk"></a>Contenuto dell'SDK

Nella tabella seguente viene descritto il contenuto di Windows Media Gestione dispositivi SDK. Tutti i file o le cartelle sono descritti in relazione al percorso di installazione dell'SDK radice.



| File                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Cartella di primo livello per Windows Media Gestione dispositivi SDK. Questa cartella include il makefile per la compilazione di tutte le applicazioni di esempio.                                                                                                                                                                                                                                                                                                              |
| IDL\\                      | Cartella che contiene tutti i file IDL necessari per compilare le intestazioni necessarie per i metodi Windows Media Gestione dispositivi. Tuttavia, invece di usare questi file, è possibile usare i file di intestazione specificati nella \\ cartella Inc.<br/> Per visualizzare un elenco di questi file IDL e per scoprire quali file di intestazione vengono compilati da quali file IDL, vedere [compilazione dei file IDL forniti con l'SDK](compiling-the-idl-files-supplied-with-the-sdk.md).<br/> |
| Inc. \\ ..<br/>       | Cartella che include tutte le intestazioni che definiscono le interfacce e i tipi di dati in questo SDK.                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm. h                   | Definisce tutte le interfacce dell'applicazione, le interfacce del provider di servizi, le interfacce del provider di contenuti protette, i codici di errore, le costanti, le strutture e l'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .                                                                                                                                                                                                                            |
| mswmdm \_ i. c                | Definisce l'interfaccia [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) .                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt. h                   | Definisce le strutture specifiche MTP richieste per le applicazioni che chiamano [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol).                                                                                                                                                                                                                                                                                                            |
| Resource. h                 | Definisce varie costanti di risorse usate dagli esempi di SDK.                                                                                                                                                                                                                                                                                                                                                                                         |
| SAC. h                      | Definisce i dati del canale autenticato sicuro necessari per tutte le applicazioni e i provider di servizi.                                                                                                                                                                                                                                                                                                                                                       |
| scclient. h                 | Definisce la classe [CSecureChannelClient](csecurechannelclient-class.md) richiesta da tutte le applicazioni.                                                                                                                                                                                                                                                                                                                                              |
| scserver. h                 | Definisce la classe [CSecureChannelServer](csecurechannelserver-class.md) richiesta da tutti i provider di servizi.                                                                                                                                                                                                                                                                                                                                         |
| WMDM \_ ver. h                | Informazioni facoltative sulla versione di Windows Media Gestione dispositivi.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog. h, wmdmlog \_ i. c    | Obbligatorio per le applicazioni o i provider di servizi che usano l'interfaccia [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp. h           | Obbligatorio per le applicazioni che gestiscono la misurazione del contenuto (vedere [utilizzo del contenuto di misurazione](metering-content-usage.md)).                                                                                                                                                                                                                                                                                                                                  |
| wmsstd. h                   | Definisce le macro Helper utilizzate dagli esempi di SDK.                                                                                                                                                                                                                                                                                                                                                                                                      |
| lib\\                      | Cartella che include le librerie di Windows Media Gestione dispositivi.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp. lib               | Libreria statica richiesta da tutti i provider di servizi e applicazioni Windows Media Gestione dispositivi.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto. lib              | Libreria statica richiesta da tutte le applicazioni Windows Media Gestione dispositivi e provider di servizi che utilizzano DRM.                                                                                                                                                                                                                                                                                                                                    |
| MDSP \\ ...<br/>      | Cartella che contiene il codice per un provider di servizi di esempio. Per informazioni su questo esempio, inclusa la modalità di compilazione ed esecuzione, vedere [esempio di provider di servizi](sample-service-provider.md).                                                                                                                                                                                                                                                    |
| app \\ ...<br/>      | Cartella che contiene due sottocartelle che contengono due metà del codice per un'applicazione desktop di esempio fornita con l'SDK. Per informazioni su questo esempio, inclusa la modalità di compilazione, vedere [esempio di applicazione desktop](sample-desktop-application.md).                                                                                                                                                                                      |
| DeviceKit \\ ...<br/> | Cartella che contiene una suite di strumenti per il test del dispositivo portatile mediante Windows Media Gestione dispositivi 11. Il test include l'enumerazione e il trasferimento di dispositivi e file, le funzionalità DRM e la conformità MTP. Questi strumenti hanno un proprio file di documentazione.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Introduzione**](getting-started.md)
</dt> </dl>

 

 





