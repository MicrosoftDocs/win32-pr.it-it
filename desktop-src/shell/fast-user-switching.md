---
description: Nei sistemi operativi precedenti è necessario disconnettersi da un utente prima che un altro utente possa effettuare l'accesso. A partire da Windows XP, un utente non deve disconnettersi per consentire a un altro utente di accedere.
ms.assetid: 72f99d32-184f-4f0b-bec1-6068c6e32f88
title: Cambio rapido utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d79f16ef8a1ea8c97bfb61d34dfa727f3d0cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994765"
---
# <a name="fast-user-switching"></a>Cambio rapido utente

Quando un utente accede a un computer, il sistema carica il proprio profilo. Poiché ogni utente dispone di un account utente univoco, consente a più utenti di condividere un computer. Quando un utente esegue l'accesso, le impostazioni del desktop, i file, i Preferiti e la cronologia visualizzati sono i rispettivi. non è possibile accedervi da altri utenti. Quando l'utente si disconnette, il relativo profilo viene mantenuto per la successiva esecuzione dell'accesso. Nei sistemi operativi precedenti è necessario disconnettersi da un utente prima che un altro utente possa effettuare l'accesso. A partire da Windows XP, un utente non deve disconnettersi per consentire a un altro utente di accedere. È invece possibile che più utenti accedano e passino rapidamente tra gli account aperti. Questa funzionalità viene definita *cambio rapido utente*. Il passaggio a un altro account non comporta la modifica dello stato delle applicazioni attualmente in esecuzione. Si supponga, ad esempio, che un utente consenta a un altro utente di passare al proprio account mentre il primo utente è connesso. Quando il primo utente torna al proprio account, le applicazioni sono in esecuzione e le connessioni di rete vengono mantenute. Viene pertanto visualizzato che entrambi gli utenti utilizzano contemporaneamente il computer.

Se le applicazioni sono conformi ai requisiti del logo Windows 2000, dovrebbero funzionare con il cambio rapido utente in Windows XP e nei sistemi operativi successivi. Tuttavia, è importante tenere presente questo scenario quando si sviluppa un'applicazione in modo che si comporti come previsto dagli utenti. Usare le linee guida seguenti durante la scrittura delle applicazioni:

-   Implementare la separazione del profilo vera e propria. Il sistema fornisce un'infrastruttura sottostante che supporta la separazione dei dati utente, delle impostazioni utente e delle impostazioni del computer. Utilizzare, ad esempio, la cartella **documenti** dell'utente per archiviare i dati creati dall'utente. Per individuare una directory per i dati specifici dell'applicazione, utilizzare il sistema di [cartelle noto](known-folders.md) con [**FOLDERID \_ RoamingAppData**](knownfolderid.md)) o, per i sistemi operativi precedenti, il sistema [**CSIDL**](csidl.md) con [**CSIDL \_ AppData**](csidl.md)). Usare **FOLDERID \_ LocalAppData** o **CSIDL \_ Local \_ AppData** per i dati che non devono essere disponibili per l'utente in altri computer, ad esempio i file temporanei.
-   Eseguire la registrazione per la notifica di un cambio utente. In genere, un'applicazione non deve ricevere notifiche quando si verifica l'opzione. Tuttavia, se l'applicazione deve ricevere notifiche relative a una modifica di sessione, può registrarsi per ricevere un messaggio di [**\_ \_ modifica WM WTSSESSION**](../termserv/wm-wtssession-change.md) .
-   Tenere presente le altre istanze dell'applicazione. In alcuni casi, ad esempio, un'applicazione deve scaricare un aggiornamento da Internet. L'aggiornamento può non riuscire se un altro utente esegue contemporaneamente un'istanza dell'applicazione in un'altra sessione. Anche se l'aggiornamento ha esito positivo, l'aggiornamento può causare un comportamento imprevedibile per altre istanze in esecuzione dell'applicazione. È pertanto consigliabile eseguire un aggiornamento dinamico solo se non sono in esecuzione altre istanze dell'applicazione. Prima di scaricare un aggiornamento dell'applicazione, potrebbe essere opportuno implementare un metodo che segnali tutte le istanze in esecuzione dell'applicazione per salvare i dati e uscire correttamente.

 

 
