---
description: Il sistema di gestione delle eccezioni in modalità utente fornisce supporto per i debugger sofisticati.
ms.assetid: c45a7dc6-e6b2-4fc4-9522-12d96893f4c7
title: Gestione delle eccezioni del debugger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aff6d566e8798aaf4f3113ce6d8f44a3bc71ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482741"
---
# <a name="debugger-exception-handling"></a>Gestione delle eccezioni del debugger

Il sistema di gestione delle eccezioni in modalità utente fornisce supporto per i debugger sofisticati. Se è in corso il debug del processo in cui si verifica un'eccezione, il sistema genera un evento di debug. Se il debugger usa la funzione [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) , l'evento di debug fa in modo che la funzione restituisca con un puntatore a una struttura di [**\_ eventi di debug**](/windows/win32/api/minwinbase/ns-minwinbase-debug_event) . Questa struttura contiene gli identificatori di processo e thread che possono essere utilizzati dal debugger per accedere al record di contesto del thread. La struttura contiene anche una struttura di [**\_ \_ informazioni di debug dell'eccezione**](/windows/win32/api/minwinbase/ns-minwinbase-exception_debug_info) che include una copia del record di eccezione.

Quando il sistema cerca un gestore di eccezioni, effettua due tentativi di notifica al debugger di un processo. Il primo tentativo di notifica fornisce al debugger la possibilità di gestire i punti di interruzione o le eccezioni in un singolo passaggio. Questa operazione è nota come *notifica first-chance*. L'utente può quindi inviare comandi del debugger per modificare l'ambiente del processo prima dell'esecuzione di qualsiasi gestore di eccezioni. Il secondo tentativo di inviare una notifica al debugger si verifica solo se il sistema non è in grado di trovare un gestore di eccezioni basato su frame che gestisce l'eccezione. Questo è noto come *notifica dell'ultima opportunità*. Se il debugger non gestisce l'eccezione dopo la notifica dell'ultima probabilità, il sistema termina il processo di cui è in corso il debug.

A ogni tentativo di notifica, il debugger utilizza la funzione [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) per restituire il controllo al sistema. Prima di restituire il controllo, il debugger può gestire l'eccezione e modificare lo stato del thread nel modo appropriato oppure può scegliere di non gestire l'eccezione. Utilizzando **ContinueDebugEvent**, il debugger può indicare che l'eccezione è stata gestita, nel qual caso lo stato del computer viene ripristinato e l'esecuzione del thread viene continuata nel punto in cui si è verificata l'eccezione. Il debugger può anche indicare che l'eccezione non è stata gestita, il che determina la continuazione della ricerca di un gestore di eccezioni da parte del sistema.

 

 
