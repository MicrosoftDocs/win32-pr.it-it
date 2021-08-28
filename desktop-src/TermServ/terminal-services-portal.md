---
title: Servizi Desktop remoto (Servizi Desktop remoto)
description: Desktop remoto Microsoft Servizi è un software di accesso remoto al PC che supporta l'accesso desktop remoto. Servizi Desktop remoto connette più client a un Desktop remoto host sessione Desktop remoto.
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto
- Servizi Desktop remoto Servizi Desktop remoto , home page
- Servizi terminal Vedere Servizi Desktop remoto Servizi Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525f62433c10c8c4f750a8ae1abbfa9496f2f096139c182a677c9dbf69ce4a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999902"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>Servizi Desktop remoto (Servizi Desktop remoto)

## <a name="purpose"></a>Scopo

Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 con Servizi Desktop remoto (precedentemente noto come Servizi terminal) consentono a un server di ospitare più sessioni client simultanee. Desktop remoto usa Servizi Desktop remoto per consentire l'esecuzione remota di una singola sessione. Un utente può connettersi a un server host sessione Desktop remoto (Host sessione Desktop remoto) (in precedenza noto come server terminal) usando il software client Connessione Desktop remoto (RDC). Il Connessione Web Desktop remoto estende Servizi Desktop remoto tecnologia al Web.

> [!Note]  
> Questo argomento è per sviluppatori di software. Se si cercano informazioni utente per le connessioni Desktop remoto, vedere [Connessione Desktop remoto: domande frequenti](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).

 

## <a name="where-applicable"></a>Se applicabile

Un client Connessione Desktop remoto (RDC) può esistere in diversi formati. I dispositivi hardware thin client che eseguono un sistema operativo Windows basato su connessione Desktop remoto possono eseguire il software client di Connessione Desktop remoto per connettersi a un server Host sessione Desktop remoto. Windows computer basati su UNIX, Macintosh o Windows possono eseguire software client di Connessione Desktop remoto per connettersi a un server Host sessione Desktop remoto per visualizzare applicazioni basate Windows desktop remoto. Questa combinazione di client RDC consente l'accesso Windows applicazioni basate su client da qualsiasi sistema operativo.

## <a name="developer-audience"></a>Sviluppatori

Gli sviluppatori che usano Servizi Desktop remoto devono avere familiarità con i linguaggi di programmazione C e C++ e con l'Windows di programmazione basato su Windows. È necessaria familiarità con l'architettura client/server. Il Connessione Web Desktop remoto include interfacce che possono essere create e distribuite tramite script all'interno di Servizi Desktop remoto web.

## <a name="run-time-requirements"></a>Requisiti di runtime

Le applicazioni che usano Servizi Desktop remoto richiedono Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 o Windows Vista. Per usare Connessione Web Desktop remoto funzionalità, l'Servizi Desktop remoto client richiede Internet Explorer e una connessione al World Wide Web. Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della pagina di riferimento per tale elemento.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Desktop remoto ActiveX controllo](remote-desktop-activex-control.md)
</dt> <dd>

Viene descritto come usare il controllo Desktop remoto ActiveX controllo .

</dd> <dt>

[Remote Desktop Protocol Provider API](custom-remote-desktop-protocols.md)
</dt> <dd>

Usare l'API Remote Desktop Protocol Provider per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.

</dd> <dt>

[Servizi Desktop remoto canali virtuali](terminal-services-virtual-channels.md)
</dt> <dd>

*I canali virtuali* sono estensioni software che possono essere usate per aggiungere miglioramenti funzionali a un Servizi Desktop remoto applizione.

</dd> <dt>

[RemoteFX API Di reindirizzamento dei supporti](remotefx-api.md)
</dt> <dd>

L RemoteFX'API Di reindirizzamento multimediale viene usata in una sessione Desktop remoto per identificare le aree del server che visualizzano contenuto in rapida evoluzione, ad esempio video. Questo contenuto può quindi essere codificato tramite video e inviato al client in formato codificato.

</dd> <dt>

[API client Connessione Desktop remoto Broker](connection-broker-client-api.md)
</dt> <dd>

Descrive come usare l'API client Connessione Desktop remoto Broker.

</dd> <dt>

[Informazioni di riferimento sulle API dell'agente attività desktop personale](task-agent-api-reference.md)
</dt> <dd>

L'API dell'agente attività desktop personale viene usata per gestire gli aggiornamenti pianificati per un desktop virtuale personale.

</dd> <dt>

[Informazioni Servizi Desktop remoto](about-terminal-services.md)
</dt> <dd>

Servizi Desktop remoto (noto in precedenza come Servizi terminal) offre funzionalità simili a un ambiente host centralizzato o mainframe basato su terminali in cui più terminali si connettono a un computer host.

</dd> <dt>

[provider Desktop remoto Management Services](rdms-api-reference.md)
</dt> <dd>

Il provider Desktop remoto Management Services (RDMS) gestisce gli ambienti VDI (Virtual Desktop Infrastructure).

</dd> <dt>

[Servizi Desktop remoto riferimento](terminal-services-reference.md)
</dt> <dd>

Documentazione dei metodi di proprietà che è possibile usare per esaminare e configurare Servizi Desktop remoto proprietà utente. Servizi Desktop remoto sono documentate anche funzioni, strutture e Connessione Web Desktop remoto di script.

</dd> <dt>

[Servizi Desktop remoto tasti di scelta rapida](terminal-services-shortcut-keys.md)
</dt> <dd>

Elenco dei tasti di scelta Servizi Desktop remoto tasti di scelta rapida.

</dd> <dt>

[Servizi Desktop remoto provider WMI](terminal-services-wmi-provider.md)
</dt> <dd>

Il Servizi Desktop remoto WMI fornisce l'accesso a livello di codice alle informazioni e alle impostazioni esposte dallo snap-in Servizi Desktop remoto Configuration/Connections Microsoft Management Console (MMC).

</dd> <dt>

[Uso di Servizi Desktop remoto](using-terminal-services.md)
</dt> <dd>

Come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia Servizi Desktop remoto (in precedenza nota come Servizi terminal) al Web usando Connessione Web Desktop remoto.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi terminal è ora disponibile Servizi Desktop remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




