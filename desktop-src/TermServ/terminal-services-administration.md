---
title: Amministrazione di Servizi Desktop remoto
description: L'API Servizi Desktop remoto consente di enumerare e gestire host sessione Desktop remoto server Host sessione Desktop remoto, sessioni client e processi.
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e763a652335c85931225746334bc21db0e6e086d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300142"
---
# <a name="remote-desktop-services-administration"></a>Amministrazione di Servizi Desktop remoto

L'API Servizi Desktop remoto consente di enumerare e gestire host sessione Desktop remoto server Host sessione Desktop remoto, sessioni client e processi.

Per recuperare i nomi di tutti i server Host sessione Desktop remoto in un dominio, chiamare la funzione [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) per enumerare i server del tipo SV di \_ tipo \_ TERMINALSERVER. Per aprire un handle per un server Host sessione Desktop remoto specifico, passare il nome del server in una chiamata alla funzione [**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) . Al termine dell'utilizzo dell'handle, rilasciarlo chiamando la funzione [**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver) .

È possibile usare l'handle restituito da **WTSOpenServer** per eseguire le operazioni seguenti sul server.



| Funzione                                                         | Operazione                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Disconnette il client da una sessione specificata. La sessione rimane attiva e l'utente può eseguire di nuovo l'accesso per connettersi alla stessa sessione.                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Restituisce un elenco di sessioni nel server Host sessione Desktop remoto specificato.                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Restituisce un elenco di processi nel server Host sessione Desktop remoto specificato.                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Disconnette la sessione specificata.                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Restituisce informazioni sulla sessione specificata nel server Host sessione Desktop remoto specificato.                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Visualizza una finestra di messaggio sulla visualizzazione client di una sessione specificata.                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Arresta e, facoltativamente, riavvia un server Host sessione Desktop remoto specificato.                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Termina un processo specificato in un server Host sessione Desktop remoto specificato.                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Apre un handle per la fine del server di un canale virtuale specificato. Per ulteriori informazioni sui canali virtuali, vedere [utilizzo di Servizi Desktop remoto canali virtuali](using-terminal-services-virtual-channels.md). |
| [**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Attende un evento, ad esempio la creazione di una sessione client o l'accesso di un utente al server Host sessione Desktop remoto.                                                                                                  |



 

Molte di queste funzioni allocano buffer per restituire informazioni al chiamante. Al termine dell'utilizzo del buffer, liberarlo chiamando la funzione [**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory) .

 

 