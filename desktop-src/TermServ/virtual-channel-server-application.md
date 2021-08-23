---
title: Applicazione server del canale virtuale
description: Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (Host sessione Desktop remoto). Si noti che è necessario fornire un metodo per avviare l'applicazione server.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63a758f4860a0ab606f18c4a5086d305b1f627475bf7bab588648cea8aabd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423565"
---
# <a name="virtual-channel-server-application"></a>Applicazione server del canale virtuale

Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (Host sessione Desktop remoto). Si noti che è necessario fornire un metodo per avviare l'applicazione server. È possibile eseguire questa operazione in diversi modi. Ad esempio, è possibile usare uno script di accesso o un programma o uno script nella cartella Startup. Gli utenti possono anche avviare l'applicazione.

È necessario archiviare il nome dell'applicazione server del canale virtuale nel Registro di sistema aggiungendo una sottochiave nel percorso seguente:

**HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Control** \\ **Terminal Server** \\ **Addins**

Per altre informazioni sulla sottochiave , vedere Monitoring [Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).

L'applicazione server può chiamare [**la funzione WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) per aprire un handle a un canale virtuale. L'applicazione può quindi usare l'handle in una delle funzioni seguenti.

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Chiude un handle di canale virtuale aperto.

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Elimina tutti i dati di input in coda inviati dal client al server in un canale virtuale specifico.

> [!Note]  
> Questa funzione non viene attualmente usata da Servizi Desktop remoto.

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Elimina tutti i dati di output in coda inviati dal server al client in un canale virtuale specifico.

> [!Note]  
> Questa funzione non viene attualmente usata da Servizi Desktop remoto.

 

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Restituisce informazioni su un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Legge i dati dall'estremità del server di un canale virtuale.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Scrive i dati sul server finale di un canale virtuale.

</dd> </dl>

 

 




