---
title: Informazioni su Servizi Desktop remoto
description: Servizi Desktop remoto (precedentemente noto come servizi Terminal) fornisce funzionalità simili a quelle di un ambiente basato su terminale, centralizzato o mainframe, in cui più terminali si connettono a un computer host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298853"
---
# <a name="about-remote-desktop-services"></a>Informazioni su Servizi Desktop remoto

Servizi Desktop remoto (precedentemente noto come servizi Terminal) fornisce funzionalità simili a quelle di un ambiente basato su terminale, centralizzato o mainframe, in cui più terminali si connettono a un computer host. Ogni terminale fornisce un canale per l'input e l'output tra un utente e il computer host. Un utente può accedere a un terminale e quindi eseguire applicazioni nel computer host, accedere a file, database, risorse di rete e così via. Ogni sessione terminal è indipendente, con il sistema operativo host che gestisce i conflitti tra più utenti che tendono a condividere le risorse condivise.

La differenza principale tra Servizi Desktop remoto e l'ambiente mainframe tradizionale è che i terminali muti in un ambiente mainframe forniscono solo input e output basati su caratteri. Un client o un emulatore di Connessione Desktop remoto (RDC) fornisce un'interfaccia utente grafica completa che include un desktop del sistema operativo Windows e il supporto per un'ampia gamma di dispositivi di input, ad esempio una tastiera e un mouse.

Nell'ambiente Servizi Desktop remoto, un'applicazione viene eseguita interamente nel server di host sessione Desktop remoto (host sessione Desktop remoto), in precedenza noto come Terminal Server. Il client RDC non esegue alcuna elaborazione locale del software dell'applicazione. Il server trasmette l'interfaccia utente grafica al client. Il client trasmette di nuovo l'input dell'utente al server.

Per ulteriori informazioni, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Modificare il reindirizzamento dei dispositivi predefinito](modify-device-redirection-default-.md)
</dt> <dd>

Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client tramite a un server host sessione Desktop remoto, potrebbe essere necessario disabilitare questa impostazione predefinita in alcuni casi.

</dd> <dt>

[Remote Desktop Protocol](remote-desktop-protocol.md)
</dt> <dd>

Il protocollo Desktop remoto Microsoft (RDP) fornisce funzionalità di visualizzazione e input Remote sulle connessioni di rete per le applicazioni basate su Windows in esecuzione in un server.

</dd> <dt>

[API Servizi Desktop remoto](terminal-services-api.md)
</dt> <dd>

L'API Servizi Desktop remoto è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto l'amministrazione.

</dd> <dt>

[Applicazioni di gestione Servizi Desktop remoto](terminal-services-management-applications.md)
</dt> <dd>

Descrive le applicazioni di gestione supportate da Servizi Desktop remoto.

</dd> <dt>

[Linee guida per la programmazione Servizi Desktop remoto](terminal-services-programming-guidelines.md)
</dt> <dd>

Argomenti che forniscono linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.

</dd> <dt>

[Sessioni di Desktop remoto](terminal-services-sessions.md)
</dt> <dd>

Poiché ogni accesso a un client di Connessione Desktop remoto (RDC) riceve un ID sessione separato, l'esperienza utente è simile a quella di essere connessi contemporaneamente a più computer; ad esempio, un computer Office e un computer di casa.

</dd> <dt>

[Connessione Web Desktop remoto](remote-desktop-web-connection.md)
</dt> <dd>

Viene descritto come installare un Connessione Web Desktop remoto.

</dd> <dt>

[Risorse in un server di host sessione Desktop remoto](resources-on-a-terminal-server.md)
</dt> <dd>

Più utenti possono accedere simultaneamente a un singolo server Host sessione Desktop remoto, condividendo le risorse hardware e software del server.

</dd> <dt>

[Novità di Servizi Desktop remoto](what-s-new-in-terminal-services.md)
</dt> <dd>

Argomenti che descrivono le modifiche apportate a ogni versione dell'API Servizi Desktop remoto.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connettersi a un altro computer utilizzando Connessione Desktop remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




