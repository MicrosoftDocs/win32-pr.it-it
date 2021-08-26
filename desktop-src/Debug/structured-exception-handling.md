---
description: Un'eccezione è un evento che si verifica durante l'esecuzione di un programma e richiede l'esecuzione di codice al di fuori del normale flusso di controllo.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Gestione strutturata delle eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c07e3bce1c15120f5bba8f4423d96a32495dcdab0262957980f2b829ac0fa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059011"
---
# <a name="structured-exception-handling"></a>Gestione strutturata delle eccezioni

*Un'eccezione* è un evento che si verifica durante l'esecuzione di un programma e richiede l'esecuzione di codice al di fuori del normale flusso di controllo. Esistono due tipi di eccezioni: eccezioni hardware ed eccezioni software. *Le eccezioni hardware* vengono avviate dalla CPU. Possono derivare dall'esecuzione di determinate sequenze di istruzioni, ad esempio la divisione per zero o il tentativo di accedere a un indirizzo di memoria non valido. *Le eccezioni software* vengono avviate in modo esplicito dalle applicazioni o dal sistema operativo. Ad esempio, il sistema può rilevare quando viene specificato un valore di parametro non valido.

*La gestione strutturata delle eccezioni* è un meccanismo per la gestione delle eccezioni hardware e software. Di conseguenza, il codice gestirà le eccezioni hardware e software in modo identico. La gestione strutturata delle eccezioni consente di avere il controllo completo sulla gestione delle eccezioni, fornisce supporto per i debugger ed è utilizzabile in tutti i linguaggi e i computer di programmazione. *La gestione delle eccezioni vettoriale* è un'estensione alla gestione strutturata delle eccezioni.

Il sistema supporta anche la gestione della *terminazione*, che consente di assicurarsi che ogni volta che viene eseguito un corpo sorvegliato di codice, viene eseguito anche un blocco di codice di terminazione specificato. Il codice di terminazione viene eseguito indipendentemente dal modo in cui il flusso di controllo lascia il corpo sorvegliato. Ad esempio, un gestore di terminazione può garantire che le attività di pulizia vengano eseguite anche se si verifica un'eccezione o un altro errore durante l'esecuzione del corpo sorvegliato del codice.

-   [Informazioni sulla gestione strutturata delle eccezioni](about-structured-exception-handling.md)
-   [Uso della gestione strutturata delle eccezioni](using-structured-exception-handling.md)
-   [Informazioni di riferimento sulla gestione strutturata delle eccezioni](structured-exception-handling-reference.md)

 

 



