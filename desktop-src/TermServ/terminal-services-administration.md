---
title: Servizi Desktop remoto amministrazione
description: L Servizi Desktop remoto API consente di enumerare e gestire Desktop remoto server Host sessione Desktop remoto, sessioni client e processi.
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46df6277b924d25608b3c4def5074c1f156738e23d114de075af01521953e7d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000281"
---
# <a name="remote-desktop-services-administration"></a>Servizi Desktop remoto amministrazione

L Servizi Desktop remoto API consente di enumerare e gestire Desktop remoto server Host sessione Desktop remoto, sessioni client e processi.

Per recuperare i nomi di tutti i server Host sessione Desktop remoto in un dominio, chiamare la funzione [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) per enumerare i server di tipo \_ \_ SV TERMINALSERVER. Per aprire un handle per un server Host sessione Desktop remoto specifico, passare il nome del server in una chiamata alla [**funzione WTSOpenServer.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) Dopo aver terminato di usare l'handle, rilasciarlo chiamando la [**funzione WTSCloseServer.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)

È possibile utilizzare l'handle restituito **da WTSOpenServer** per eseguire le operazioni seguenti nel server.



| Funzione                                                         | Operazione                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Disconnette il client da una sessione specificata. La sessione rimane attiva e l'utente può accedere nuovamente per connettersi alla stessa sessione.                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Restituisce un elenco di sessioni nel server Host sessione Desktop remoto specificato.                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Restituisce un elenco di processi nel server Host sessione Desktop remoto specificato.                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Disconnette la sessione specificata.                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Restituisce informazioni sulla sessione specificata nel server Host sessione Desktop remoto specificato.                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Visualizza una finestra di messaggio nella visualizzazione client di una sessione specificata.                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Arresta e facoltativamente riavvia un server Host sessione Desktop remoto specificato.                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Termina un processo specificato in un server Host sessione Desktop remoto specificato.                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Apre un handle all'estremità server di un canale virtuale specificato. Per altre informazioni sui canali virtuali, vedere [Uso Servizi Desktop remoto canali virtuali.](using-terminal-services-virtual-channels.md) |
| [**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Attende un evento, ad esempio la creazione di una sessione client o un utente che accede al server Host sessione Desktop remoto.                                                                                                  |



 

Molte di queste funzioni allocano buffer per restituire informazioni al chiamante. Dopo aver terminato di usare il buffer, liberarlo chiamando la [**funzione WTSFreeMemory.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)

 

 