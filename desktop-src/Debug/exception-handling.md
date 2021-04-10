---
description: Le eccezioni possono essere avviate dall'hardware o dal software e possono essere eseguite in modalità kernel, oltre che come codice in modalità utente. La gestione strutturata delle eccezioni fornisce un singolo meccanismo per la gestione delle eccezioni in modalità kernel e utente.
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: Gestione delle eccezioni (gestione degli errori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb44cd294d89be81862c5330dda5b14811add1f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125706"
---
# <a name="exception-handling-error-handling"></a>Gestione delle eccezioni (gestione degli errori)

Le eccezioni possono essere avviate dall'hardware o dal software e possono essere eseguite in modalità kernel, oltre che come codice in modalità utente. La gestione strutturata delle eccezioni fornisce un singolo meccanismo per la gestione delle eccezioni in modalità kernel e utente.

L'esecuzione di determinate sequenze di istruzioni può causare eccezioni avviate dall'hardware. Una violazione di accesso, ad esempio, viene generata dall'hardware quando un processo tenta di leggere o scrivere in un indirizzo virtuale a cui non dispone dell'accesso appropriato.

Gli eventi che richiedono la gestione delle eccezioni possono verificarsi anche durante l'esecuzione di una routine software, ad esempio quando viene specificato un valore di parametro non valido. Quando ciò accade, un thread può avviare un'eccezione in modo esplicito chiamando la funzione [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) . Questa funzione consente al thread chiamante di specificare le informazioni che descrivono l'eccezione.

Un'eccezione può essere continua o non continua. Un'eccezione non continuabile si verifica quando l'evento non è continuabile nell'hardware oppure se la continuazione non è sensata. Un'eccezione non continua non termina l'applicazione. Pertanto, un'applicazione potrebbe essere in grado di intercettare l'eccezione ed eseguire. Tuttavia, un'eccezione non continuabile si presenta in genere a causa di uno stack danneggiato o di un altro problema grave, rendendo difficile il recupero dall'eccezione.

 

 
