---
description: Utilizzare la registrazione eventi per registrare gli errori che si verificano nella DLL delle prestazioni.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Gestione degli errori nella DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967516"
---
# <a name="error-handling-in-the-dll"></a>Gestione degli errori nella DLL

Utilizzare la registrazione eventi per registrare gli errori che si verificano nella DLL delle prestazioni. La registrazione degli eventi di errore contribuisce alla risoluzione dei problemi relativi alle applicazioni che forniscono dati sulle prestazioni durante lo sviluppo e dopo l'installazione. È necessario limitare la quantità di registrazione degli errori che si verifica nella funzione [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) perché la raccolta dei dati può essere frequente.

Se si verificano problemi con la funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) , il sistema registra gli errori seguenti nel registro eventi. Se si verifica uno degli errori seguenti, il sistema non chiama di nuovo la DLL delle prestazioni. La DLL viene invece scaricata.

-   **Perflib \_ Impossibile \_ \_ \_ trovare il processo di apertura**: registrato quando il nome della stored procedure definito nel registro di sistema non è stato trovato nella dll come funzione esportata. Questo problema si verifica in genere quando la DLL o il servizio non è installato correttamente o il nome della funzione è stato rinominato senza aggiornare la procedura di installazione.
-   **Perflib \_ Errore di apertura \_ proc \_**: registrato quando la procedura di apertura restituisce uno stato di errore diverso da Error \_ Success. In tal caso, è necessario che nella DLL sia stata immessa anche una voce del registro eventi che descrive le condizioni che hanno causato l'errore.
-   **Perflib \_ Apri \_ \_ eccezione proc**: registrato quando la procedura di apertura rileva un'eccezione non gestita. Questo problema si verifica in genere a causa di una condizione di errore imprevista rilevata dalla procedura di apertura.

 

 
