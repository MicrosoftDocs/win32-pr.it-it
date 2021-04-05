---
title: Applicazione Virtual Channel Server
description: Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (host sessione Desktop remoto). Si noti che è necessario fornire un metodo per avviare l'applicazione server.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711413"
---
# <a name="virtual-channel-server-application"></a>Applicazione Virtual Channel Server

Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (host sessione Desktop remoto). Si noti che è necessario fornire un metodo per avviare l'applicazione server. Questa operazione può essere eseguita in diversi modi. ad esempio, è possibile usare uno script di accesso o un programma o uno script nella cartella di avvio. Gli utenti possono anche avviare l'applicazione.

È necessario archiviare il nome dell'applicazione Virtual Channel Server nel registro di sistema aggiungendo una sottochiave nel percorso seguente:

**HKEY \_ \_** \\  \\  \\  \\ **Terminal Server** \\ **componenti aggiuntivi** del controllo CurrentControlSet di sistema del computer locale

Per ulteriori informazioni sulla sottochiave, vedere [monitoraggio delle connessioni di sessione e disconnessione](monitoring-session-connections-and-disconnections.md).

L'applicazione server può chiamare la funzione [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) per aprire un handle per un canale virtuale. L'applicazione può quindi usare l'handle in una delle funzioni seguenti.

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Chiude un handle di canale virtuale aperto.

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Elimina tutti i dati di input in coda inviati dal client al server su un canale virtuale specifico.

> [!Note]  
> Questa funzione attualmente non viene utilizzata da Servizi Desktop remoto.

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Elimina tutti i dati di output in coda inviati dal server al client su un canale virtuale specifico.

> [!Note]  
> Questa funzione attualmente non viene utilizzata da Servizi Desktop remoto.

 

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Restituisce informazioni su un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Legge i dati dall'estremità server di un canale virtuale.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Scrive i dati nell'entità finale del server di un canale virtuale.

</dd> </dl>

 

 




