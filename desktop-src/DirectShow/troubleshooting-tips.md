---
description: Suggerimenti per la risoluzione dei problemi
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Suggerimenti per la risoluzione dei problemi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313401"
---
# <a name="troubleshooting-tips"></a>Suggerimenti per la risoluzione dei problemi

I suggerimenti seguenti consentono di evitare deadlock o arresti anomali dell'applicazione DirectShow.

**Oggetti globali**

Un oggetto C++ globale non deve creare oggetti DirectShow nel metodo del costruttore o rilasciarli nel metodo del distruttore. In questo modo l'applicazione può bloccarsi per un periodo illimitato, per il motivo seguente:

Impossibile chiudere i thread all'interno di una funzione del punto di ingresso della DLL. Il kernel 32 include un blocco globale del processo durante la funzione del punto di ingresso e il blocco impedisce la chiusura del thread. Poiché alcuni oggetti DirectShow sono proprietari di thread, possono bloccarsi se rilasciati dall'interno di una funzione del punto di ingresso della DLL. Se un'applicazione dispone di un oggetto C++ globale, la DLL di runtime C chiama il distruttore dell'oggetto quando la DLL viene scaricata. Se il distruttore rilascia oggetti DirectShow, può bloccarsi di conseguenza.

Per motivi simili, una DLL non deve creare o rilasciare oggetti DirectShow nella relativa routine del punto di ingresso.

**Rilascio di interfacce**

È consigliabile rilasciare tutti i puntatori dell'interfaccia DirectShow mentre l'applicazione sta ancora elaborando i messaggi, prima di uscire dal ciclo di messaggi. In caso contrario, è possibile che vengano visualizzate varie asserzioni perché alcuni oggetti DirectShow inviano messaggi durante le routine di pulizia.

(Come corollario, se si utilizza la classe ATL **CWindowImpl** , non attendere che **OnFinalMessage** non liberi le interfacce. Liberarli invece quando si gestisce il messaggio di \_ chiusura WM.

**Conteggi dei riferimenti**

Quando la versione di debug di Quartz.dll viene scaricata, verifica se gli oggetti DirectShow hanno conteggi dei riferimenti che non sono stati rilasciati. In tal caso, viene generata un'asserzione:


```C++
g_cFGObjects == 0 
```



Quando l'asserzione ha esito negativo, significa che l'applicazione ha perso un conteggio dei riferimenti. Esaminare il codice e assicurarsi di rilasciare tutti i puntatori di interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



