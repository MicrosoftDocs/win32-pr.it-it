---
description: Quando si verifica un'eccezione hardware o software, il processore arresta l'esecuzione nel punto in cui si è verificata l'eccezione e trasferisce il controllo al sistema.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Invio di eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b7b4f73c9d2c3fbaf15b4390ee6ecc6b9aa06b50524ec080fc45319d3b94767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912731"
---
# <a name="exception-dispatching"></a>Invio di eccezioni

Quando si verifica un'eccezione hardware o software, il processore arresta l'esecuzione nel punto in cui si è verificata l'eccezione e trasferisce il controllo al sistema. In primo luogo, il sistema salva lo stato del computer del thread corrente e le informazioni che descrivono l'eccezione. Il sistema tenta quindi di trovare un gestore eccezioni per gestire l'eccezione.

Lo stato del computer del thread in cui si è verificata l'eccezione viene salvato in una [**struttura CONTEXT.**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Queste informazioni (denominate *record di* contesto ) consentono al sistema di continuare l'esecuzione nel punto dell'eccezione se l'eccezione viene gestita correttamente. La descrizione dell'eccezione ( denominata **record dell'eccezione**) viene salvata in una [**struttura EXCEPTION \_ RECORD.**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Poiché archivia le informazioni dipendenti dal computer del record di contesto separatamente dalle informazioni indipendenti dal computer del record di eccezione, il meccanismo di gestione delle eccezioni è portabile a piattaforme diverse.

Le informazioni nei record di contesto e di eccezione sono disponibili tramite la [**funzione GetExceptionInformation**](getexceptioninformation.md) e possono essere rese disponibili per qualsiasi gestore di eccezioni eseguito come risultato dell'eccezione. Il record dell'eccezione include le informazioni seguenti.

-   Codice di eccezione che identifica il tipo di eccezione.
-   Flag che indicano se l'eccezione è continuabile. Qualsiasi tentativo di continuare l'esecuzione dopo un'eccezione non concisa genera un'altra eccezione.
-   Puntatore a un altro record di eccezione. Ciò semplifica la creazione di un elenco collegato di eccezioni se si verificano eccezioni annidate.
-   Indirizzo in corrispondenza del quale si è verificata l'eccezione.
-   Matrice di argomenti che forniscono informazioni aggiuntive sull'eccezione.

Quando si verifica un'eccezione nel codice in modalità utente, il sistema usa l'ordine di ricerca seguente per trovare un gestore eccezioni:

1.  Se il processo è in fase di debug, il sistema invia una notifica al debugger. Per altre informazioni, vedere [Gestione delle eccezioni del debugger](debugger-exception-handling.md).
2.  Se il processo non è in fase di debug o se il debugger associato non gestisce l'eccezione, il sistema tenta di individuare un gestore di eccezioni basato su frame eseguendo una ricerca negli stack frame del thread in cui si è verificata l'eccezione. Il sistema cerca prima il stack frame corrente, quindi esegue la ricerca negli stack frame precedenti in ordine inverso.
3.  Se non è possibile trovare alcun gestore basato su frame o nessun gestore basato su frame gestisce l'eccezione, ma il processo è in fase di debug, il sistema invia una seconda notifica al debugger.
4.  Se il processo non è in fase di debug o se il debugger associato non gestisce l'eccezione, il sistema fornisce la gestione predefinita in base al tipo di eccezione. Per la maggior parte delle eccezioni, l'azione predefinita è chiamare la [**funzione ExitProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)

Quando si verifica un'eccezione nel codice in modalità kernel, il sistema cerca gli stack frame dello stack del kernel nel tentativo di individuare un gestore eccezioni. Se non è possibile trovare un gestore o nessun gestore gestisce l'eccezione, il sistema viene arrestato come se fosse stata chiamata la funzione [**ExitWindows.**](/windows/win32/api/winuser/nf-winuser-exitwindows)

 

 
