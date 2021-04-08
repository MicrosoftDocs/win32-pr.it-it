---
description: Un'eccezione è un evento che si verifica durante l'esecuzione di un programma e richiede l'esecuzione di codice al di fuori del normale flusso di controllo.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Gestione strutturata delle eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877318"
---
# <a name="structured-exception-handling"></a>Gestione strutturata delle eccezioni

Un' *eccezione* è un evento che si verifica durante l'esecuzione di un programma e richiede l'esecuzione di codice al di fuori del normale flusso di controllo. Esistono due tipi di eccezioni: eccezioni hardware ed eccezioni software. Le *eccezioni hardware* vengono avviate dalla CPU. Possono derivare dall'esecuzione di determinate sequenze di istruzioni, ad esempio la divisione per zero o un tentativo di accedere a un indirizzo di memoria non valido. Le *eccezioni software* vengono avviate in modo esplicito dalle applicazioni o dal sistema operativo. Ad esempio, il sistema è in grado di rilevare quando viene specificato un valore di parametro non valido.

La *gestione strutturata delle eccezioni* è un meccanismo per gestire le eccezioni hardware e software. Il codice gestirà pertanto le eccezioni hardware e software in modo identico. La gestione strutturata delle eccezioni consente di avere il controllo completo sulla gestione delle eccezioni, fornisce il supporto per i debugger ed è utilizzabile in tutti i linguaggi di programmazione e nei computer. La *gestione delle eccezioni con vettori* è un'estensione della gestione strutturata delle eccezioni.

Il sistema supporta anche la *gestione della terminazione*, che consente di garantire che ogni volta che viene eseguito un corpo sorvegliato del codice venga eseguito anche un blocco di codice di terminazione specificato. Il codice di terminazione viene eseguito indipendentemente dal modo in cui il flusso di controllo lascia il corpo sorvegliato. Un gestore di terminazione può ad esempio garantire che le attività di pulizia vengano eseguite anche se si verifica un'eccezione o un altro errore durante l'esecuzione del corpo sorvegliato del codice.

-   [Informazioni sulla gestione delle eccezioni strutturata](about-structured-exception-handling.md)
-   [Uso della gestione strutturata delle eccezioni](using-structured-exception-handling.md)
-   [Guida di riferimento alla gestione delle eccezioni strutturata](structured-exception-handling-reference.md)

 

 



