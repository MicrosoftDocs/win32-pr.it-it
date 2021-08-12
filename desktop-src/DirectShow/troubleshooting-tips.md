---
description: Suggerimenti per la risoluzione dei problemi
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Suggerimenti per la risoluzione dei problemi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fe361af291c29f8784235066f341d940ab38205cd3b8238896011f85021a9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651243"
---
# <a name="troubleshooting-tips"></a>Suggerimenti per la risoluzione dei problemi

I suggerimenti seguenti consentono di evitare deadlock o arresti anomali nell DirectShow applizione.

**Oggetti globali**

Un oggetto C++ globale non deve creare DirectShow oggetti nel metodo costruttore né rilasciarli nel metodo del distruttore. In questo modo l'applicazione può bloccarsi a tempo indeterminato, per il motivo seguente:

I thread non possono uscire mentre si trova all'interno della funzione del punto di ingresso di una DLL. Il kernel 32 contiene un blocco del processo globale durante la funzione del punto di ingresso e impedisce la chiusura del thread. Poiché alcuni oggetti DirectShow thread, possono bloccarsi se rilasciati dall'interno di una funzione del punto di ingresso DLL. Se un'applicazione ha un oggetto C++ globale, la DLL di runtime C chiama il distruttore dell'oggetto quando la DLL viene scaricata. Se il distruttore rilascia DirectShow oggetti, può bloccarsi di conseguenza.

Per motivi simili, una DLL non deve creare o rilasciare DirectShow oggetti nella routine del punto di ingresso.

**Rilascio di interfacce**

È necessario rilasciare tutti DirectShow puntatori a interfaccia mentre l'applicazione sta ancora elaborando i messaggi, prima di uscire dal ciclo di messaggi. In caso contrario, potrebbero essere disponibili diverse asserzioni, perché alcuni DirectShow inviano messaggi durante le routine di pulizia.

Come corollario, se si usa la classe **ATL CWindowImpl,** non attendere **finché OnFinalMessage** non libera le interfacce. Al contrario, liberarle quando si gestisce il messaggio WM \_ CLOSE.

**Conteggi dei riferimenti**

Quando la versione di debug Quartz.dll scarica, verifica se gli oggetti DirectShow hanno conteggi di riferimento che non sono stati rilasciati. In tal caso, genera un'asserzione:


```C++
g_cFGObjects == 0 
```



Quando questa asserzione ha esito negativo, significa che l'applicazione ha generato un conteggio dei riferimenti. Esaminare il codice e assicurarsi di rilasciare tutti i puntatori a interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



