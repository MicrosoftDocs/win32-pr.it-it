---
title: Windows Glossario dell'animazione
description: Questo glossario contiene termini e acronimi di interesse per gli sviluppatori che usano Windows Animation Manager.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Windows Animazione Windows animazione , glossario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb477edcaa49aa8baff1bc628ca5d94c13dacc0e552137275ff1e92d8e4cfae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137394"
---
# <a name="windows-animation-glossary"></a>Windows Glossario dell'animazione

Questo glossario contiene termini e acronimi di interesse per gli sviluppatori che usano Windows Animation Manager.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animazione** 
</dt> <dd>

Sequenza di immagini fisse sintetiche e successive che genera un'ira di movimento quando viene riprodotta.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Gestione animazione** 
</dt> <dd>

Componente principale dell'Windows e dell'interfaccia programmatica centrale per la gestione (creazione, pianificazione e controllo) delle animazioni.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**timer di animazione**
</dt> <dd>

Componente per fornire servizi di temporizzazione che possono essere usati insieme al gestore dell'animazione. La frequenza dei fotogrammi viene limitato dinamicamente in base al carico dell'applicazione e del sistema o in modalità a basso consumo. Vedere anche: limitazione delle richieste.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variabile di animazione** 
</dt> <dd>

Valore che può essere animato. Le variabili di animazione possono essere usate per rappresentare la posizione, le dimensioni, la rotazione, la trasparenza e altre qualità degli oggetti visibili.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**Cancellazione**
</dt> <dd>

Processo di rimozione di uno storyboard dalla pianificazione prima dell'avvio della riproduzione.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**Compressione**
</dt> <dd>

Distorcendo la percezione del tempo di uno storyboard. Il sistema aumenta la frequenza con cui lo storyboard avanza passando i valori di ora di input che aumentano più velocemente del clock di sistema.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**Conclusione**
</dt> <dd>

Processo di indirizzamento di uno storyboard per uscire da qualsiasi ciclo indefinito. Se il ciclo è iniziato, l'iterazione corrente verrà completata e verrà riprodotto il resto dello storyboard. In caso contrario, la parte a ciclo continuo dello storyboard verrà ignorata completamente.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**frame** 
</dt> <dd>

Singola immagine in un film o in un'animazione.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**frequenza dei fotogrammi** 
</dt> <dd>

Numero di fotogrammi visualizzati al secondo. Frequenze fotogrammi più elevate producono in genere un movimento più uniforme nell'immagine.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**Interpolatore**
</dt> <dd>

Oggetto di programmazione che esegue l'interpolazione matematica del valore e della velocità di una variabile per una transizione.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**Fotogramma chiave**
</dt> <dd>

Momento all'interno di uno storyboard, che può essere specificato in relazione all'inizio dello storyboard, a un altro fotogramma chiave o all'ora di fine di una transizione e usato per specificare l'ora di inizio e di fine di altre transizioni o di un ciclo all'interno dello storyboard.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**Ciclo**
</dt> <dd>

Sezione di uno storyboard tra due fotogrammi chiave riprodotti ripetutamente. Un ciclo può riprodurre un numero finito di volte o per un periodo illimitato.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**confronto di priorità** 
</dt> <dd>

Codice definito dal client che confronta due storyboard, uno già pianificato e l'altro che sta per essere pianificato, per determinarne la priorità relativa. Uno storyboard pianificato può essere tagliato, compresso, annullato o terminato per abilitare la pianificazione dello storyboard con priorità più alta.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**storyboard** 
</dt> <dd>

Gruppo di transizioni di animazione sincronizzate l'una rispetto all'altra.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**tag** 
</dt> <dd>

Coppia costituita da un ID integer e da un oggetto COM utilizzato da un'applicazione per identificare le variabili e gli storyboard di animazione nell'ambito di un gestore di animazione specifico.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**limitazione delle richieste** 
</dt> <dd>

Regolazione dinamica della frequenza dei fotogrammi di un'animazione per soddisfare determinati requisiti. La limitazione consente di garantire che il rendering delle animazioni sia eseguito a una frequenza dei fotogrammi coerente, riducendo al minimo l'uso delle risorse di sistema per il rendering a una velocità superiore a quella necessaria o utile.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**tick** 
</dt> <dd>

Evento timer che in genere attiva il rendering di un singolo frame.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transizione** 
</dt> <dd>

Costrutto che definisce gli aggiornamenti progressivi per una variabile di animazione in un periodo di tempo.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**Taglio**
</dt> <dd>

Precedenza del controllo di uno storyboard di una variabile di animazione con uno storyboard con priorità più alta. Se il trimming di uno storyboard in una o più variabili causa la chiusura prematura dello storyboard, viene considerato troncato. Vedere anche: troncamento.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**Troncamento**
</dt> <dd>

Termina uno storyboard prematuramente eliminando il controllo di una o più variabili a cui viene animata con uno o più storyboard con priorità più alta. Vedere anche: trimming.

</dd> </dl>

 

 




