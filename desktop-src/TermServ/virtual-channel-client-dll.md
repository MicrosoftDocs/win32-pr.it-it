---
title: DLL client canale virtuale
description: Il client di un'applicazione di canali virtuali è una DLL caricata durante l'inizializzazione del Servizi Desktop remoto nel computer client. La DLL deve essere registrata nel computer client.
ms.assetid: fca0505c-c4a9-4230-aeaa-ff3dfa62f581
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd7ffccda8b1da7dfc3920b0a47a12e97840e0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044775"
---
# <a name="virtual-channel-client-dll"></a>DLL client canale virtuale

Il client di un'applicazione di canali virtuali è una DLL caricata durante l'inizializzazione del Servizi Desktop remoto nel computer client. La DLL deve essere registrata nel computer client. Per ulteriori informazioni, vedere [registrazione client del canale virtuale](virtual-channel-client-registration.md).

La DLL client deve esportare una funzione [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) , che Servizi Desktop remoto chiama durante l'inizializzazione. Il punto di ingresso **VirtualChannelEntry** riceve un puntatore a una struttura di [**punti di \_ ingresso \_ del canale**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points) . Questa struttura contiene i puntatori alle funzioni che la DLL client chiama per accedere ai canali virtuali.



| Funzione                                                      | Descrizione                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)<br/>   | Registra i nomi dei canali virtuali che devono essere utilizzati dal client e fornisce una funzione di callback [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) tramite la quale Servizi Desktop remoto notifica al client gli eventi che influiscono sulla connessione client.<br/> |
| [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)<br/>   | Apre l'estremità client di un canale virtuale specificato e fornisce una funzione di callback [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) tramite la quale Servizi Desktop remoto notifica al client gli eventi che influiscono sul canale virtuale.<br/>                    |
| [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)<br/> | Scrive i dati in un canale virtuale. Servizi Desktop remoto invia questi dati all'estremità server del canale virtuale. Il termine server chiama la funzione [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) per leggere i dati.<br/>                                             |
| [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)<br/> | Chiude un canale virtuale.<br/>                                                                                                                                                                                                                                                  |



 

La funzione [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) della dll deve chiamare la funzione [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) per inizializzare l'accesso ai canali virtuali. Quando si chiama **VirtualChannelInit**, è necessario passare un puntatore alla funzione di callback [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) . Servizi Desktop remoto chiama questa funzione di callback quando l'inizializzazione è completa e di nuovo quando viene stabilita una connessione con un server di host sessione Desktop remoto (host sessione Desktop remoto).

Una volta stabilita la connessione, è possibile chiamare la funzione [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) per aprire i canali virtuali registrati dalla chiamata [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) . La chiamata **VirtualChannelOpen** specifica un puntatore alla funzione di callback [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) .

Dopo la restituzione della chiamata a [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) , è possibile chiamare la funzione [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite) per scrivere sul canale virtuale. L'operazione di scrittura è asincrona, pertanto non è necessario liberare o riutilizzare il buffer passato a **VirtualChannelWrite** fino a quando Servizi Desktop remoto chiama la funzione [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) per indicare che l'operazione di scrittura è stata completata. Quando si chiama **VirtualChannelWrite**, è possibile passare una parte di dati utente che identifica l'operazione di scrittura. Servizi Desktop remoto passa nuovamente i dati utente quando chiama **VirtualChannelOpenEvent** per notificare che l'operazione è stata completata. Sul lato server del canale virtuale, il componente aggiuntivo del server chiama la funzione [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) per leggere i dati.

Servizi Desktop remoto chiama anche la funzione [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) quando i dati vengono scritti nel canale virtuale dal modulo server. Il modulo server chiama la funzione [**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite) per scrivere i dati nell'entità finale del canale virtuale del server.

I moduli client e server possono scrivere blocchi di dati di qualsiasi dimensione nel canale virtuale. Prima di inviare i dati, tuttavia, Servizi Desktop remoto segmenta i dati in blocchi di byte di lunghezza del blocco del canale \_ \_ . Servizi Desktop remoto chiama la funzione [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) una volta per ogni blocco di dati, anziché ricompilare i dati in un blocco di dimensioni originali. Ogni chiamata a **VirtualChannelOpenEvent** indica le dimensioni del blocco, la dimensione totale scritta dal server e se i dati costituiscono l'inizio, il centro o la fine di un blocco scritto dal server.

È possibile chiamare la funzione [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose) per chiudere un canale. Tuttavia, non è necessario chiamarlo perché Servizi Desktop remoto chiude automaticamente tutti i canali quando il client si disconnette dal server.

 

 





