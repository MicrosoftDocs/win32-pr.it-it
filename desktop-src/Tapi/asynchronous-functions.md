---
description: Un'operazione che viene completata in modo asincrono esegue una parte della relativa elaborazione nella chiamata di funzione effettuata dall'applicazione e il resto in un thread di esecuzione indipendente dopo che TAPI 2. x ha restituito dalla chiamata di funzione.
ms.assetid: 37b544e4-6413-4741-b8b6-ec676ce4ca97
title: Funzioni asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e792a4b1d6a25a4f49fbb2abe2c19ce3071ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314639"
---
# <a name="asynchronous-functions"></a>Funzioni asincrone

Un'operazione che viene completata in modo asincrono esegue una parte della relativa elaborazione nella chiamata di funzione effettuata dall'applicazione e il resto in un thread di esecuzione indipendente dopo che TAPI 2. x ha restituito dalla chiamata di funzione. Per garantire il completamento dell'elaborazione della chiamata, il provider di servizi Vector la richiesta a un'altra entità attiva nel sistema, ad esempio un server LAN, hardware del componente aggiuntivo, un'opzione o una rete, e quindi torna all'applicazione. A questo punto, all'applicazione viene restituito un errore negativo o un identificatore di richiesta positivo.

Al momento del completamento asincrono (il provider di servizi ha ricevuto un interrupt dall'hardware, ovvero un messaggio deve essere recapitato), il provider di servizi chiama TAPISRV e segnala che "l'evento *X* è appena avvenuto. Recapitare un messaggio appropriato a tutte le applicazioni interessate ". Quando TAPISRV riceve questo messaggio, inoltra il messaggio alla libreria a collegamento dinamico TAPI, nel processo dell'applicazione, che a sua volta invia un messaggio di finestra, segnala un handle di evento o Invia un post a una porta di completamento di I/O, in base allo schema di notifica del messaggio selezionato dall'applicazione in [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) o [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa).

Quando la parte asincrona dell'operazione viene completata, all'applicazione viene inviato un messaggio di [**\_ risposta di riga**](./line-reply.md) o [**\_ risposta telefonica**](./phone-reply.md). Questo messaggio contiene, come uno dei relativi parametri, l'identificatore della richiesta restituito dalla chiamata di funzione. Questo identificatore di richiesta consente all'applicazione di determinare quale richiesta originale è stata completata. (Le applicazioni devono ricordare gli identificatori di richiesta di tutte le richieste in corso, in modo che i messaggi di risposta possano essere gestiti correttamente). Un secondo parametro per il messaggio di risposta di riga \_ (o \_ risposta telefonica) è il valore restituito asincrono. Si tratta di un valore negativo (per un errore) o zero se l'operazione è stata completata correttamente. Per le operazioni asincrone, è possibile che i valori restituiti vengano restituiti come parte della funzione Return o come parametro *dwParam2* nel messaggio di risposta di riga \_ o di \_ risposta telefonica. Il valore 0, che indica l'esito positivo, verrà restituito solo nel \_ messaggio di risposta di riga e mai come valore restituito della funzione.

Le funzioni Initialize ( [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) e [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa)) indicano a TAPI come inviare questi messaggi all'applicazione.

> [!Note]  
> In alcuni casi, se un'applicazione multithreading chiama una funzione asincrona da un thread diverso da quello da cui l'applicazione ha inizializzato la linea o il dispositivo telefonico, l'applicazione può ricevere il messaggio di [**\_ risposta di riga**](./line-reply.md) o [**telefono \_**](./phone-reply.md) prima della restituzione della funzione asincrona. In questi casi, l'applicazione deve salvare i parametri del messaggio e attendere il completamento della funzione asincrona e l'identificatore della richiesta è noto prima dell'elaborazione del messaggio.

 

 

 
