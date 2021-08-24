---
title: Informazioni Servizi Desktop remoto
description: Servizi Desktop remoto (precedentemente noto come Servizi terminal) offre funzionalità simili a un ambiente basato su terminale, host centralizzato o mainframe, in cui più terminali si connettono a un computer host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto , about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680ccae3d8944c92d64da526831142d662ac5dc38157c741cf8f5426768fc745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681461"
---
# <a name="about-remote-desktop-services"></a>Informazioni Servizi Desktop remoto

Servizi Desktop remoto (precedentemente noto come Servizi terminal) offre funzionalità simili a un ambiente basato su terminale, host centralizzato o mainframe, in cui più terminali si connettono a un computer host. Ogni terminale fornisce un conduit per l'input e l'output tra un utente e il computer host. Un utente può accedere a un terminale e quindi eseguire applicazioni nel computer host, accedendo a file, database, risorse di rete e così via. Ogni sessione del terminale è indipendente e il sistema operativo host gestisce i conflitti tra più utenti che si contendono le risorse condivise.

La differenza principale tra Servizi Desktop remoto e l'ambiente mainframe tradizionale è che i terminali in un ambiente mainframe forniscono solo input e output basati su caratteri. Un client Connessione Desktop remoto (RDC) o un emulatore fornisce un'interfaccia utente grafica completa che include un desktop del sistema operativo Windows e il supporto per un'ampia gamma di dispositivi di input, ad esempio tastiera e mouse.

Nell'Servizi Desktop remoto, un'applicazione viene eseguita interamente nel server Host sessione Desktop remoto (host sessione Desktop remoto) (precedentemente noto come server terminal). Il client RDC non esegue alcuna elaborazione locale del software applicativo. Il server trasmette l'interfaccia utente grafica al client. Il client trasmette l'input dell'utente al server.

Per ulteriori informazioni, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Modificare il valore predefinito di Reindirizzamento dispositivo](modify-device-redirection-default-.md)
</dt> <dd>

Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client a un server host sessione Desktop remoto, in alcuni casi potrebbe essere necessario disabilitare questa impostazione predefinita.

</dd> <dt>

[Remote Desktop Protocol](remote-desktop-protocol.md)
</dt> <dd>

Il protocollo RDP (Desktop remoto Microsoft Protocol) offre funzionalità remote di visualizzazione e input su connessioni di rete per Windows applicazioni basate su Windows in esecuzione in un server.

</dd> <dt>

[API Servizi Desktop remoto](terminal-services-api.md)
</dt> <dd>

L Servizi Desktop remoto aPI è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto amministrazione.

</dd> <dt>

[Servizi Desktop remoto applicazioni di gestione](terminal-services-management-applications.md)
</dt> <dd>

Vengono descritte le applicazioni di Servizi Desktop remoto supportate da .

</dd> <dt>

[Servizi Desktop remoto linee guida per la programmazione](terminal-services-programming-guidelines.md)
</dt> <dd>

Argomenti che forniscono linee guida per lo sviluppo di applicazioni in Servizi Desktop remoto ambiente.

</dd> <dt>

[Desktop remoto sessioni](terminal-services-sessions.md)
</dt> <dd>

Poiché ogni accesso a un client Connessione Desktop remoto (RDC) riceve un ID sessione separato, l'esperienza utente è simile all'accesso a più computer contemporaneamente; ad esempio un computer dell'ufficio e un computer domestico.

</dd> <dt>

[Connessione Web Desktop remoto](remote-desktop-web-connection.md)
</dt> <dd>

Viene descritto come installare un Connessione Web Desktop remoto.

</dd> <dt>

[Risorse in un server host Desktop remoto sessione](resources-on-a-terminal-server.md)
</dt> <dd>

Più utenti possono accedere contemporaneamente a un singolo server Host sessione Desktop remoto, condividendo le risorse hardware e software del server.

</dd> <dt>

[Novità di Servizi Desktop remoto](what-s-new-in-terminal-services.md)
</dt> <dd>

Argomenti che descrivono le modifiche in ogni versione dell'API Servizi Desktop remoto.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a un altro computer usando Connessione Desktop remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




