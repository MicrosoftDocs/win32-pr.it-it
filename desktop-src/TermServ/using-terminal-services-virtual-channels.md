---
title: Uso di Servizi Desktop remoto canali virtuali
description: Per implementare un canale virtuale, fornire i moduli server e client dell'applicazione di un canale virtuale.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708752"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>Uso di Servizi Desktop remoto canali virtuali

Per implementare un canale virtuale, fornire i moduli server e client dell'applicazione di un canale virtuale. Il modulo server può essere un'applicazione in modalità utente o un driver in modalità kernel. Il modulo client deve essere una DLL.

Per le descrizioni di questi moduli, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Applicazione Virtual Channel Server](virtual-channel-server-application.md)
</dt> <dd>

Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (host sessione Desktop remoto). Si noti che è necessario fornire un metodo per avviare l'applicazione server.

</dd> <dt>

[DLL client canale virtuale](virtual-channel-client-dll.md)
</dt> <dd>

Il client di un'applicazione di canali virtuali è una DLL caricata durante l'inizializzazione del Servizi Desktop remoto nel computer client. La DLL deve essere registrata nel computer client.

</dd> <dt>

[Registrazione client del canale virtuale](virtual-channel-client-registration.md)
</dt> <dd>

È necessario archiviare il nome della DLL client nel registro di sistema.

</dd> <dt>

[Canale virtuale persistente del controllo remoto](remote-control-persistent-virtual-channels.md)
</dt> <dd>

Un canale virtuale persistente del controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client. I dati continueranno a essere trasmessi e ricevuti tramite questo canale.

</dd> <dt>

[Canali virtuali dinamici](dynamic-virtual-channels.md)
</dt> <dd>

Le API del canale virtuale dinamico (DVC) estendono le API del canale virtuale esistente per Servizi Desktop remoto, note come API del canale virtuale statico (SVC).

</dd> </dl>

Se è stata abilitata l'applicazione di un canale virtuale nella distribuzione di Servizi Desktop remoto, è anche possibile rendere disponibile l'applicazione ai computer client che accedono al server Host sessione Desktop remoto tramite il controllo ActiveX Desktop remoto. Per ulteriori informazioni, vedere [utilizzo del controllo ActiveX Desktop remoto con i canali virtuali](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




