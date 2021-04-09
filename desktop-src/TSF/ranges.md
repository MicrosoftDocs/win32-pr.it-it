---
title: Intervalli
description: Intervalli
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Framework servizi di testo (TSF), intervalli
- TSF (Framework di servizi di testo), intervalli
- Servizi di testo, intervalli
- Applicazioni abilitate per TSF, intervalli
- ranges
- Framework servizi di testo (TSF), ancoraggi
- TSF (Framework di servizi di testo), ancoraggi
- Servizi di testo, ancoraggi
- Applicazioni abilitate per TSF, ancoraggi
- ancoraggi
- Framework servizi di testo (TSF), cloni
- TSF (Framework di servizi di testo), cloni
- Servizi di testo, cloni
- Applicazioni abilitate per TSF, cloni
- cloni
- Framework servizi di testo (TSF), backup
- TSF (Framework di servizi di testo), backup
- Servizi di testo, backup
- Applicazioni abilitate per TSF, backup
- backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955810"
---
# <a name="ranges"></a>Intervalli

## <a name="anchors"></a>Ancoraggi

Un intervallo è delimitato da due *ancoraggi*, un ancoraggio iniziale e un ancoraggio finale. Un ancoraggio esiste in uno slot immaginario tra due caratteri. L'ancoraggio iniziale si riferisce al testo che segue l'ancoraggio e l'ancoraggio finale è correlato al testo che precede l'ancoraggio. Entrambi gli ancoraggi di inizio e fine possono esistere nella stessa posizione. In questo caso, l'intervallo ha una lunghezza pari a zero.

Ad esempio, iniziare con il testo seguente:


```C++
This is text.
```



Applicare ora un intervallo al testo con entrambi gli ancoraggi iniziale e finale nella posizione 0. Viene rappresentato visivamente come segue:


```C++
<anchor></anchor>This is text.
```



Gli ancoraggi non prendono spazio all'interno del testo stesso. Si tratta di un intervallo di lunghezza zero e il testo è vuoto.

A questo punto, spostare l'ancoraggio finale + 3 posizioni. Viene rappresentato visivamente come segue:


```C++
<anchor>Thi</anchor>s is text.
```



L'ancoraggio iniziale è posizionato immediatamente prima del carattere nella posizione 0 e l'ancoraggio finale è posizionato subito dopo il carattere nella posizione 3 perché l'ancoraggio finale è stato spostato a destra di 3 posizioni. L'intervallo di testo è ora "Thi".

Inoltre, l'ancoraggio iniziale non può essere eseguito per seguire l'ancoraggio finale e non è possibile fare in modo che preceda l'ancoraggio iniziale.

## <a name="anchor-gravity"></a>Gravità ancoraggio

Ogni ancoraggio ha un'impostazione di *gravità* che determina il modo in cui l'ancoraggio risponde quando il testo viene inserito nel flusso di testo nella posizione di ancoraggio. Quando viene eseguito un inserimento in corrispondenza della posizione di un ancoraggio, è necessario apportare una modifica nella posizione dell'ancoraggio. La gravità determina il modo in cui viene apportata la regolazione della posizione di ancoraggio.

Ad esempio:


```C++
It is <anchor></anchor>cold today.
```



Se la parola "very" viene inserita nella posizione dell'intervallo, l'ancoraggio iniziale può essere posizionato prima o dopo la parola inserita:


```C++
It is <anchor>very </anchor>cold today.
```



\- oppure -


```C++
It is very <anchor></anchor>cold today.
```



La gravità di ancoraggio specifica il modo in cui l'ancoraggio viene riposizionato quando viene eseguito un inserimento nella relativa posizione. La gravità può essere *indietro* o *Avanti*.

Se l'ancoraggio presenta una gravità precedente, l'ancoraggio si sposta indietro rispetto al punto di inserimento, in caso di inserimento, in modo che il testo inserito segua l'ancoraggio:


```C++
It is <anchor>very </anchor>cold today.
```



Se l'ancoraggio ha una gravità in avanti, l'ancoraggio si sposta in avanti rispetto al punto di inserimento, in modo che il testo inserito preceda l'ancoraggio:


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a>Cloni e backup

Esistono due modi per creare una copia di un oggetto Range. Il primo consiste nel creare un *Clone* dell'intervallo usando [ITfRange:: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone). Il secondo consiste nell'eseguire un *backup* dell'intervallo usando [ITfContext:: CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).

Un clone è una copia di un intervallo che non include dati statici. Gli ancoraggi dell'intervallo vengono copiati, ma il clone copre ancora un intervallo di testo all'interno del contesto. Un clone è un oggetto Range in tutti gli aspetti. Ciò significa che il testo e le proprietà di un intervallo clonato sono dinamici e verranno modificati se il testo e/o le proprietà dell'intervallo coperto dal clone cambiano.

Un backup archivia il testo e le proprietà di un intervallo nel momento in cui il backup viene eseguito come dati statici. Un backup clona anche l'intervallo originale in modo che sia possibile tenere traccia delle modifiche apportate alle dimensioni e alla posizione dell'intervallo originale. Ciò significa che il testo e le proprietà di un intervallo di cui è stato eseguito il backup sono statici e non cambiano se il testo e/o le proprietà dell'intervallo coperto dal backup cambiano.

Ad esempio, l'intervallo seguente (pRange) all'interno del contesto:


```C++
"This is some <pRange>text</pRange>."
```



A questo punto, creare un clone e un backup di questo intervallo:


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



A questo punto, gli oggetti contengono gli elementi seguenti:


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Modificare ora il testo di pRange:


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



A questo punto, gli oggetti contengono gli elementi seguenti:


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



L'impostazione del testo ha causato la modifica del testo all'interno del contesto. Ha anche causato la modifica dell'ancoraggio finale di pRange e pClone. pClone contiene ora "altre parole" perché il testo è stato modificato nell'intervallo e le modifiche vengono rilevate da tutti gli intervalli. Quando il testo coperto da pRange e pClone è stato modificato, anche il testo di pClone è cambiato.

Il testo in pBackup non è stato modificato rispetto al pRange originale perché i dati (testo e proprietà) nel backup non sono correlati al contesto e vengono archiviati separatamente. Il clone contenuto all'interno del backup cambia effettivamente, ma i dati sono statici.

Quando si ripristina un backup, il backup può essere applicato al clone all'interno del backup o a un intervallo diverso. Per applicare il backup al clone all'interno del backup, passare **null** a [ITfRangeBackup:: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , come illustrato nell'esempio di codice seguente:


```C++
pBackup->Restore(ec, NULL);
```



A questo punto, gli oggetti contengono gli elementi seguenti:


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Per ripristinare il backup in un intervallo diverso, passare un puntatore all'oggetto intervallo quando si chiama **ITfRangeBackup:: Restore**. Il testo e le proprietà di cui è stato eseguito il backup verranno applicati al nuovo intervallo. Ad esempio, usando l'esempio precedente prima della chiamata di **ripristino** , Prange verrà modificato per illustrare quanto segue:


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



A questo punto, gli oggetti contengono gli elementi seguenti:


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



Quando l'ancoraggio finale di pRange è stato spostato a sinistra di due punti, l'ancoraggio finale di pClone non è stato modificato.

A questo punto, ripristinare il backup usando pRange con l'esempio di codice seguente:


```C++
pBackup->Restore(ec, pRange);
```



A questo punto, gli oggetti contengono gli elementi seguenti:


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



Il testo coperto da pRange è stato sostituito con "Text", una parte del testo analizzata da pClone è stata modificata e pBackup cambia per trovare la corrispondenza con pRange.

 

 




