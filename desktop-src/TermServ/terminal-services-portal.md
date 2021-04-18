---
title: Servizi Desktop remoto (Servizi Desktop remoto)
description: Desktop remoto Microsoft Services è un software di accesso remoto al PC che supporta l'accesso desktop remoto. Servizi Desktop remoto connette più client a un server di host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto
- Servizi Desktop remoto Servizi Desktop remoto, home page
- Servizi Terminal vedere Servizi Desktop remoto Servizi Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300894"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>Servizi Desktop remoto (Servizi Desktop remoto)

## <a name="purpose"></a>Scopo

Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 con Servizi Desktop remoto (precedentemente noto come servizi Terminal) consentono a un server di ospitare più sessioni client simultanee. Desktop remoto usa la tecnologia Servizi Desktop remoto per consentire l'esecuzione remota di una singola sessione. Un utente può connettersi a un server di host sessione Desktop remoto (host sessione Desktop remoto) (in precedenza noto come Terminal Server) utilizzando il software client Connessione Desktop remoto (RDC). Il Connessione Web Desktop remoto estende la tecnologia Servizi Desktop remoto al Web.

> [!Note]  
> Questo argomento è per gli sviluppatori di software. Per informazioni sull'utente per le connessioni Desktop remoto, vedere [Connessione desktop remoto: domande frequenti](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).

 

## <a name="where-applicable"></a>Se applicabile

Un client Connessione Desktop remoto (RDC) può esistere in un'ampia gamma di moduli. I dispositivi hardware thin client che eseguono un sistema operativo basato su Windows incorporato possono eseguire il software client RDC per connettersi a un server Host sessione Desktop remoto. I computer basati su Windows, Macintosh o UNIX possono eseguire il software client RDC per connettersi a un server Host sessione Desktop remoto per visualizzare le applicazioni basate su Windows. Questa combinazione di client RDC consente di accedere alle applicazioni basate su Windows praticamente da qualsiasi sistema operativo.

## <a name="developer-audience"></a>Sviluppatori

Gli sviluppatori che utilizzano Servizi Desktop remoto devono acquisire familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione basato su Windows. È necessaria una certa familiarità con l'architettura client/server. Il Connessione Web Desktop remoto include interfacce di script per la creazione e la distribuzione di canali virtuali tramite script all'interno di Servizi Desktop remoto applicazioni Web.

## <a name="run-time-requirements"></a>Requisiti di runtime

Le applicazioni che usano Servizi Desktop remoto richiedono Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 o Windows Vista. Per utilizzare Connessione Web Desktop remoto funzionalità, l'applicazione client Servizi Desktop remoto richiede Internet Explorer e una connessione al World Wide Web. Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Controllo ActiveX Desktop remoto](remote-desktop-activex-control.md)
</dt> <dd>

Viene descritto come utilizzare il controllo ActiveX Desktop remoto.

</dd> <dt>

[API del provider Remote Desktop Protocol](custom-remote-desktop-protocols.md)
</dt> <dd>

Usare l'API del provider Remote Desktop Protocol per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.

</dd> <dt>

[Servizi Desktop remoto canali virtuali](terminal-services-virtual-channels.md)
</dt> <dd>

I *canali virtuali* sono estensioni software che possono essere usate per aggiungere miglioramenti funzionali a un'applicazione Servizi Desktop remoto.

</dd> <dt>

[API di reindirizzamento dei supporti RemoteFX](remotefx-api.md)
</dt> <dd>

L'API di reindirizzamento dei supporti RemoteFX viene utilizzata in una sessione di Desktop remoto per identificare le aree del server in cui viene visualizzato il contenuto a modifica rapida, ad esempio il video. Questo contenuto può quindi essere codificato come video e inviato al client in formato codificato.

</dd> <dt>

[API client di Connessione Desktop remoto broker](connection-broker-client-api.md)
</dt> <dd>

Viene descritto come utilizzare l'API client di Connessione Desktop remoto broker.

</dd> <dt>

[Informazioni di riferimento sull'API personal desktop Task Agent](task-agent-api-reference.md)
</dt> <dd>

L'API personal desktop Task Agent viene utilizzata per gestire gli aggiornamenti pianificati a un desktop virtuale personale.

</dd> <dt>

[Informazioni su Servizi Desktop remoto](about-terminal-services.md)
</dt> <dd>

Servizi Desktop remoto (precedentemente noto come servizi Terminal) fornisce funzionalità simili a quelle di un ambiente basato su terminale, centralizzato o mainframe, in cui più terminali si connettono a un computer host.

</dd> <dt>

[Provider di Desktop remoto Management Services](rdms-api-reference.md)
</dt> <dd>

Il provider Desktop remoto Management Services (RDBMS) gestisce gli ambienti VDI (Virtual Desktop Infrastructure).

</dd> <dt>

[Riferimento Servizi Desktop remoto](terminal-services-reference.md)
</dt> <dd>

Documentazione dei metodi di proprietà che è possibile utilizzare per esaminare e configurare Servizi Desktop remoto proprietà utente. Sono inoltre documentate le funzioni di Servizi Desktop remoto, le strutture e le interfacce Connessione Web Desktop remoto con script.

</dd> <dt>

[Tasti di scelta rapida Servizi Desktop remoto](terminal-services-shortcut-keys.md)
</dt> <dd>

Elenco di tasti di scelta rapida Servizi Desktop remoto.

</dd> <dt>

[Provider WMI Servizi Desktop remoto](terminal-services-wmi-provider.md)
</dt> <dd>

Il provider WMI Servizi Desktop remoto fornisce accesso a livello di codice alle informazioni e alle impostazioni esposte dallo snap-in Microsoft Management Console (MMC) Servizi Desktop remoto Configuration/Connections.

</dd> <dt>

[Utilizzo di Servizi Desktop remoto](using-terminal-services.md)
</dt> <dd>

Come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia di Servizi Desktop remoto (precedentemente nota come servizi Terminal) al Web utilizzando Connessione Web Desktop remoto.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi terminal è ora Servizi Desktop remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




