---
title: Glossario animazione Windows
description: Questo glossario contiene i termini e gli acronimi di interesse per gli sviluppatori che utilizzano Windows Animation Manager.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Animazione Windows animazione Windows, Glossario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b7f276b0f20efc35057a9ee7c006c3cf170ac3
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2019
ms.locfileid: "104516558"
---
# <a name="windows-animation-glossary"></a>Glossario animazione Windows

Questo glossario contiene i termini e gli acronimi di interesse per gli sviluppatori che utilizzano Windows Animation Manager.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animazione** di 
</dt> <dd>

Sequenza di immagini ancora sintetiche e successive che producono un illusione di spostamento quando vengono riprodotte.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Gestione animazioni** 
</dt> <dd>

Componente principale dell'animazione Windows e dell'interfaccia centrale a livello di codice per la gestione (creazione, pianificazione e controllo) di animazioni.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**timer animazione**
</dt> <dd>

Componente per fornire servizi di temporizzazione che possono essere utilizzati in combinazione con gestione animazioni. Limita dinamicamente la frequenza dei fotogrammi in base al carico del sistema e dell'applicazione o in modalità a basso consumo. Vedere anche: limitazione delle richieste.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variabile di animazione** 
</dt> <dd>

Valore che può essere animato. Le variabili di animazione possono essere utilizzate per rappresentare la posizione, le dimensioni, la rotazione, la trasparenza e altre qualità degli oggetti visibili.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**annullamento**
</dt> <dd>

Processo di rimozione di uno storyboard dalla pianificazione prima che venga avviata la riproduzione.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**compressione**
</dt> <dd>

Distorsione della percezione del tempo di uno storyboard. Il sistema aumenta la velocità con cui lo storyboard avanza passando i valori di tempo di input che aumentano più velocemente rispetto al clock di sistema.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**conclusione**
</dt> <dd>

Il processo di indirizzamento di uno storyboard alla chiusura di tutti i cicli indefiniti. Se il ciclo è iniziato, l'iterazione corrente verrà completata e il resto dello storyboard verrà riprodotto. In caso contrario, la parte con ciclo dello storyboard verrà ignorata interamente.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**frame** 
</dt> <dd>

Una singola immagine in un film o un'animazione.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**frequenza fotogrammi** 
</dt> <dd>

Numero di frame visualizzati al secondo. Le frequenze dei fotogrammi più elevate in genere producono un movimento più uniforme nell'immagine.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolatore**
</dt> <dd>

Oggetto di programmazione che esegue l'interpolazione matematica del valore e della velocità di una variabile per una transizione.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**fotogramma chiave**
</dt> <dd>

Un momento nel tempo all'interno di uno storyboard, che può essere specificato in relazione all'inizio dello storyboard, relativo a un altro fotogramma chiave o all'ora di fine di una transizione, e utilizzato per specificare l'ora di inizio e di fine di altre transizioni o un ciclo all'interno dello storyboard.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**ciclo**
</dt> <dd>

Sezione di uno storyboard tra due fotogrammi chiave riprodotti ripetutamente. Un ciclo può essere riprodotto per un numero finito di volte o per un periodo illimitato.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**confronto di priorità** 
</dt> <dd>

Codice definito dal client che confronta due storyboard, uno già pianificato e l'altro che sta per essere pianificato, per determinarne la priorità relativa. Uno storyboard pianificato può essere tagliato, compresso, annullato o terminato per consentire la pianificazione dello storyboard con priorità più elevata.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**storyboard** 
</dt> <dd>

Un gruppo di transizioni di animazioni sincronizzate l'una rispetto all'altra.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**tag** di 
</dt> <dd>

Coppia costituita da un ID di tipo integer e da un oggetto COM utilizzato da un'applicazione per identificare le variabili di animazione e gli storyboard nell'ambito di un gestore di animazioni specifico.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**limitazione delle richieste** 
</dt> <dd>

Regolazione dinamica della frequenza dei fotogrammi di un'animazione per soddisfare determinati requisiti. La limitazione consente di garantire il rendering delle animazioni con una frequenza dei fotogrammi coerente, riducendo al minimo l'uso delle risorse di sistema per il rendering a una velocità superiore a quella necessaria o utile.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**casella** di selezione 
</dt> <dd>

Evento timer che in genere attiva il rendering di un singolo frame.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transizione** 
</dt> <dd>

Costrutto che definisce gli aggiornamenti progressivi per una variabile di animazione in un periodo di tempo.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**taglio**
</dt> <dd>

Annullamento del controllo di una variabile di animazione con uno storyboard con priorità maggiore. Se la rimozione di uno storyboard in una o più variabili comporta la chiusura anomala dello storyboard, viene considerata troncata. Vedere anche: troncamento.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**troncamento**
</dt> <dd>

Terminazione anticipata di uno storyboard con l'interruzione del controllo di una o più variabili che anima con uno o più storyboard con priorità più alta. Vedere anche: trimming.

</dd> </dl>

 

 




