---
description: Le eccezioni possono essere avviate da hardware o software e possono verificarsi sia in modalità kernel che in codice in modalità utente. La gestione strutturata delle eccezioni offre un unico meccanismo per la gestione delle eccezioni in modalità kernel e in modalità utente.
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: Gestione delle eccezioni (gestione degli errori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253776619100095ae1ba9c92fa2caa373bc950bdf6725c6ef5d0239520320bd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260871"
---
# <a name="exception-handling-error-handling"></a>Gestione delle eccezioni (gestione degli errori)

Le eccezioni possono essere avviate da hardware o software e possono verificarsi sia in modalità kernel che in codice in modalità utente. La gestione strutturata delle eccezioni offre un unico meccanismo per la gestione delle eccezioni in modalità kernel e in modalità utente.

L'esecuzione di determinate sequenze di istruzioni può comportare eccezioni avviate dall'hardware. Ad esempio, una violazione di accesso viene generata dall'hardware quando un processo tenta di leggere o scrivere in un indirizzo virtuale a cui non ha l'accesso appropriato.

Gli eventi che richiedono la gestione delle eccezioni possono verificarsi anche durante l'esecuzione di una routine software, ad esempio quando viene specificato un valore di parametro non valido. In questo caso, un thread può avviare un'eccezione in modo esplicito chiamando la [**funzione RaiseException.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) Questa funzione consente al thread chiamante di specificare informazioni che descrivono l'eccezione.

Un'eccezione può essere continuabile o non costante. Un'eccezione non costante si verifica quando l'evento non è continuabile nell'hardware o se la continuazione non ha senso. Un'eccezione non concisa non termina l'applicazione. Di conseguenza, un'applicazione potrebbe essere in grado di rilevare l'eccezione ed eseguirlo. Tuttavia, un'eccezione non concisa si verifica in genere a causa di uno stack danneggiato o di un altro problema grave, rendendo difficile il ripristino dall'eccezione.

 

 
