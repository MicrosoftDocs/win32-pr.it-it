---
description: Quando si verifica un'eccezione hardware o software, il processore interrompe l'esecuzione nel punto in cui si è verificata l'eccezione e trasferisce il controllo al sistema.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Invio di eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02b40aa132541fe88d692cbbf1881a8b620a209
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125712"
---
# <a name="exception-dispatching"></a>Invio di eccezioni

Quando si verifica un'eccezione hardware o software, il processore interrompe l'esecuzione nel punto in cui si è verificata l'eccezione e trasferisce il controllo al sistema. In primo luogo, il sistema salva lo stato del computer del thread corrente e le informazioni che descrivono l'eccezione. Il sistema tenta quindi di trovare un gestore di eccezioni per gestire l'eccezione.

Lo stato del computer del thread in cui si è verificata l'eccezione viene salvato in una struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) . Queste informazioni, denominate *record di contesto*, consentono al sistema di continuare l'esecuzione nel punto dell'eccezione se l'eccezione viene gestita correttamente. La descrizione dell'eccezione (denominata **record eccezione**) viene salvata in una struttura [**di \_ record di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_record) . Poiché archivia le informazioni dipendenti dal computer del record di contesto separatamente dalle informazioni indipendenti dal computer del record di eccezione, il meccanismo di gestione delle eccezioni è portabile su piattaforme diverse.

Le informazioni nei record di contesto e di eccezione sono disponibili tramite la funzione [**GetExceptionInformation**](getexceptioninformation.md) e possono essere rese disponibili per tutti i gestori di eccezioni eseguiti come risultato dell'eccezione. Il record di eccezione include le informazioni seguenti.

-   Codice di eccezione che identifica il tipo di eccezione.
-   Flag che indicano se l'eccezione è continuabile. Qualsiasi tentativo di continuare l'esecuzione dopo un'eccezione non continua genera un'altra eccezione.
-   Puntatore a un altro record di eccezione. In questo caso si semplifica la creazione di un elenco collegato di eccezioni se si verificano eccezioni nidificate.
-   Indirizzo in corrispondenza del quale si è verificata l'eccezione.
-   Matrice di argomenti che forniscono informazioni aggiuntive sull'eccezione.

Quando si verifica un'eccezione nel codice in modalità utente, il sistema usa l'ordine di ricerca seguente per trovare un gestore di eccezioni:

1.  Se è in corso il debug del processo, il sistema invia una notifica al debugger. Per ulteriori informazioni, vedere [gestione delle eccezioni del debugger](debugger-exception-handling.md).
2.  Se il processo non viene sottoposto a debug o se il debugger associato non gestisce l'eccezione, il sistema tenta di individuare un gestore di eccezioni basato su frame eseguendo una ricerca negli stack frame del thread in cui si è verificata l'eccezione. Il sistema cerca prima la stack frame corrente, quindi Cerca negli stack frame precedenti in ordine inverso.
3.  Se non è possibile trovare un gestore basato su frame oppure nessun gestore basato su frame gestisce l'eccezione, ma è in corso il debug del processo, il sistema invia una notifica al debugger una seconda volta.
4.  Se il processo non viene sottoposto a debug o se il debugger associato non gestisce l'eccezione, il sistema fornisce la gestione predefinita basata sul tipo di eccezione. Per la maggior parte delle eccezioni, l'azione predefinita consiste nel chiamare la funzione [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .

Quando si verifica un'eccezione nel codice in modalità kernel, il sistema cerca nello stack frame dello stack del kernel il tentativo di individuare un gestore di eccezioni. Se non è possibile trovare un gestore oppure nessun gestore gestisce l'eccezione, il sistema viene arrestato come se fosse stata chiamata la funzione [**ExitWindows**](/windows/win32/api/winuser/nf-winuser-exitwindows) .

 

 
