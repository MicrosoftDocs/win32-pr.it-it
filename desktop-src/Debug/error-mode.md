---
description: La modalità di errore indica al sistema come l'applicazione risponderà a errori gravi.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Modalità di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1baa4c0bc4e1209586b630f2a58bfb06572131de8e7d2706614c78646d7e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260931"
---
# <a name="error-mode"></a>Modalità di errore

La modalità di errore indica al sistema come l'applicazione risponderà a errori gravi. Gli errori gravi includono errori del disco, errori di unità non pronta, disallineamento dei dati ed eccezioni non gestite. Questa modalità di errore può essere gestita in base al thread o al processo. Un'applicazione può consentire al sistema di visualizzare una finestra di messaggio che informa l'utente che si è verificato un errore oppure può gestire gli errori.

Per gestire questi errori senza l'intervento dell'utente, [**usare SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) o [**setThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)specifico del thread. Dopo aver chiamato una di queste funzioni e specificato i flag appropriati, il sistema non visualizza le finestre di messaggio di errore corrispondenti.

Un processo può recuperare la modalità di errore [**usando GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) [**o GetThreadErrorMode.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)

È consigliabile che tutte le applicazioni chiamino la funzione [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) a livello di processo con un parametro **SEM \_ FAILCRITICALERRORS all'avvio.** In questo modo si evita che le finestre di dialogo in modalità di errore si applicino all'applicazione.

A parte questo, i chiamanti devono favorire le versioni specifiche del thread di queste funzioni poiché sono meno disaffezionate rispetto al normale comportamento del sistema.

 

 
