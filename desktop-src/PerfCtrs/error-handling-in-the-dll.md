---
description: Utilizzare la registrazione degli eventi per registrare gli errori che si verificano nella DLL delle prestazioni.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Gestione degli errori nella DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a64dcfdf360a1dcc2301b5496d3f4630631cd7bfbc3fffb0e2cd5408120351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517471"
---
# <a name="error-handling-in-the-dll"></a>Gestione degli errori nella DLL

Utilizzare la registrazione degli eventi per registrare gli errori che si verificano nella DLL delle prestazioni. La registrazione degli eventi di errore consente di risolvere i problemi delle applicazioni che forniscono dati sulle prestazioni durante lo sviluppo e dopo l'installazione. È consigliabile limitare la quantità di registrazione degli errori che si verifica nella [**funzione CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) perché la raccolta dei dati può essere frequente.

Se si verificano problemi con la funzione [**OpenPerformanceData,**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) il sistema registra gli errori seguenti nel registro eventi. Se si verifica uno degli errori seguenti, il sistema non chiama di nuovo la DLL delle prestazioni. Al contrario, la DLL viene scaricata.

-   **PERFLIB \_ OPEN \_ PROC NOT FOUND \_ \_ :** registrato quando il nome della procedura definito nel Registro di sistema non è stato trovato nella DLL come funzione esportata. Ciò si verifica in genere quando la DLL o il servizio non è installato correttamente o il nome della funzione è stato rinominato senza aggiornare la procedura di installazione.
-   **PERFLIB \_ OPEN \_ PROC \_ FAILURE :** registrato quando la procedura di apertura ha restituito uno stato di errore diverso da ERROR \_ SUCCESS. In questo caso, è necessario che la DLL abbia immesso anche una voce del registro eventi che descrive le condizioni che hanno causato l'errore.
-   **PERFLIB \_ OPEN \_ PROC \_ EXCEPTION**: registrato quando la procedura aperta rileva un'eccezione non gestita. Ciò è in genere dovuto a una condizione di errore imprevista rilevata dalla procedura aperta.

 

 
