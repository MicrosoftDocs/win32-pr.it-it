---
title: DLL del client del canale virtuale
description: Il client di un'applicazione di canali virtuali è una DLL caricata durante l'Servizi Desktop remoto inizializzazione nel computer client. La DLL deve essere registrata nel computer client.
ms.assetid: fca0505c-c4a9-4230-aeaa-ff3dfa62f581
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f9ba01db57de6dc030e6c47b09c4173156ef8f85e3969716ae6e10dfc069f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423581"
---
# <a name="virtual-channel-client-dll"></a>DLL del client del canale virtuale

Il client di un'applicazione di canali virtuali è una DLL caricata durante l'Servizi Desktop remoto inizializzazione nel computer client. La DLL deve essere registrata nel computer client. Per altre informazioni, vedere [Registrazione client del canale virtuale.](virtual-channel-client-registration.md)

La DLL client deve esportare una [**funzione VirtualChannelEntry,**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) che Servizi Desktop remoto chiamate durante l'inizializzazione. Il **punto di ingresso VirtualChannelEntry** riceve un puntatore a una struttura CHANNEL ENTRY [**\_ \_ POINTS.**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points) Questa struttura contiene puntatori alle funzioni chiamate dalla DLL client per accedere ai canali virtuali.



| Funzione                                                      | Descrizione                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)<br/>   | Registra i nomi dei canali virtuali che devono essere usati dal client e fornisce una funzione di callback [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) tramite la quale Servizi Desktop remoto notifica al client gli eventi che influiscono sulla connessione client.<br/> |
| [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)<br/>   | Apre l'estremità client di un canale virtuale specificato e fornisce una funzione di callback [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) tramite la quale Servizi Desktop remoto notifica al client gli eventi che interessano il canale virtuale.<br/>                    |
| [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)<br/> | Scrive i dati in un canale virtuale. Servizi Desktop remoto invia questi dati all'estremità server del canale virtuale. L'estremità del server [**chiama la funzione WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) per leggere i dati.<br/>                                             |
| [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)<br/> | Chiude un canale virtuale.<br/>                                                                                                                                                                                                                                                  |



 

La funzione [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) della DLL deve chiamare la [**funzione VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) per inizializzare l'accesso ai canali virtuali. Quando si chiama **VirtualChannelInit,** è necessario passare un puntatore alla funzione di callback [**VirtualChannelInitEvent.**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) Servizi Desktop remoto chiama questa funzione di callback al termine dell'inizializzazione e di nuovo quando è stata stabilita una connessione con un server Host sessione Desktop remoto (Host sessione Desktop remoto).

Dopo aver stabilito la connessione, è possibile chiamare la [**funzione VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) per aprire i canali virtuali registrati dalla [**chiamata VirtualChannelInit.**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) La **chiamata VirtualChannelOpen** specifica un puntatore alla funzione di callback [**VirtualChannelOpenEvent.**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)

Al termine [**della chiamata VirtualChannelOpen,**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) è possibile chiamare la [**funzione VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite) per scrivere nel canale virtuale. L'operazione di scrittura è asincrona, pertanto non è necessario liberare o riutilizzare il buffer passato a **VirtualChannelWrite** finché Servizi Desktop remoto non chiama la funzione [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) per indicare che l'operazione di scrittura è stata completata. Quando si chiama **VirtualChannelWrite,** è possibile passare una porzione di dati utente che identifica l'operazione di scrittura. Servizi Desktop remoto passa nuovamente questi dati utente quando chiama **VirtualChannelOpenEvent** per notificare che l'operazione è stata completata. All'estremità del server del canale virtuale, il componente aggiuntivo del server chiama la [**funzione WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) per leggere i dati.

Servizi Desktop remoto chiama anche la [**funzione VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) quando i dati vengono scritti nel canale virtuale dal modulo server. Il modulo server chiama la [**funzione WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite) per scrivere dati all'estremità server del canale virtuale.

I moduli client e server possono scrivere blocchi di dati di qualsiasi dimensione nel canale virtuale. Prima di inviare i dati, tuttavia, Servizi Desktop remoto segmenta i dati in blocchi di byte CHANNEL \_ CHUNK \_ LENGTH. Servizi Desktop remoto chiama la [**funzione VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) una volta per ogni blocco di dati, anziché ricompilare i dati in un blocco delle dimensioni originali. Ogni chiamata a **VirtualChannelOpenEvent** indica le dimensioni del blocco, le dimensioni totali scritte dal server e se i dati costituiscono l'inizio, la metà o la fine di un blocco scritto dal server.

È possibile chiamare la [**funzione VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose) per chiudere un canale. Tuttavia, non è necessario chiamarlo perché Servizi Desktop remoto chiude automaticamente tutti i canali quando il client si disconnette dal server.

 

 





