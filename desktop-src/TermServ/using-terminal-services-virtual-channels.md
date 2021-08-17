---
title: Uso Servizi Desktop remoto canali virtuali
description: Per implementare un canale virtuale, fornire i moduli server e client dell'applicazione di un canale virtuale.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f538259134d539104e55706578778931a1180a1901a9891eec7f62f1f40144b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423741"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>Uso Servizi Desktop remoto canali virtuali

Per implementare un canale virtuale, fornire i moduli server e client dell'applicazione di un canale virtuale. Il modulo server può essere un'applicazione in modalità utente o un driver in modalità kernel. Il modulo client deve essere una DLL.

Per le descrizioni di questi moduli, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Applicazione server del canale virtuale](virtual-channel-server-application.md)
</dt> <dd>

Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (Host sessione Desktop remoto). Si noti che è necessario fornire un metodo per avviare l'applicazione server.

</dd> <dt>

[DLL client del canale virtuale](virtual-channel-client-dll.md)
</dt> <dd>

Il client di un'applicazione di canali virtuali è una DLL caricata durante l Servizi Desktop remoto inizializzazione nel computer client. La DLL deve essere registrata nel computer client.

</dd> <dt>

[Registrazione client del canale virtuale](virtual-channel-client-registration.md)
</dt> <dd>

È necessario archiviare il nome della DLL client nel Registro di sistema.

</dd> <dt>

[Canali virtuali permanenti di controllo remoto](remote-control-persistent-virtual-channels.md)
</dt> <dd>

Un canale virtuale permanente di controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client. I dati continueranno a essere trasmessi e ricevuti tramite questo canale.

</dd> <dt>

[Canali virtuali dinamici](dynamic-virtual-channels.md)
</dt> <dd>

Le API DVC (Dynamic Virtual Channel) estendono le API del canale virtuale esistenti per Servizi Desktop remoto, note come API del canale virtuale statico (SVC).

</dd> </dl>

Se nella distribuzione di Servizi Desktop remoto è stata abilitata l'applicazione di un canale virtuale, è anche possibile rendere disponibile l'applicazione ai computer client che accedono al server Host sessione Desktop remoto tramite il controllo Desktop remoto ActiveX desktop remoto. Per altre informazioni, vedere [Uso del controllo Desktop remoto ActiveX con canali virtuali](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




