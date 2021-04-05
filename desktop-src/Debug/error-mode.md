---
description: La modalità di errore indica al sistema in che modo l'applicazione sta per rispondere a errori gravi.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Modalità di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125715"
---
# <a name="error-mode"></a>Modalità di errore

La modalità di errore indica al sistema in che modo l'applicazione sta per rispondere a errori gravi. Gli errori gravi includono errore del disco, errori dell'unità non pronta, allineamento dei dati e eccezioni non gestite. Questa modalità di errore può essere gestita per singolo thread o per processo. Un'applicazione può consentire al sistema di visualizzare una finestra di messaggio che informa l'utente che si è verificato un errore o che è in grado di gestire gli errori.

Per gestire questi errori senza l'intervento dell'utente, usare [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) o il [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)specifico del thread. Quando si chiama una di queste funzioni e si specificano i flag appropriati, nel sistema non vengono visualizzate le caselle di messaggio di errore corrispondenti.

Un processo può recuperare la modalità di errore utilizzando [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) o [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).

È consigliabile che tutte le applicazioni chiamino la funzione [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) a livello di processo con un parametro di **sem \_ FAILCRITICALERRORS** all'avvio. Ciò consente di evitare che le finestre di dialogo in modalità di errore appendino l'applicazione.

A parte questo, i chiamanti devono prediligere le versioni specifiche dei thread di queste funzioni perché sono meno problematiche rispetto al normale comportamento del sistema.

 

 
