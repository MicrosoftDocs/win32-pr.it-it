---
title: Interazione
description: L'interazione è la varietà di modi in cui gli utenti interagiscono con l'app, tra cui tocco, tastiera, mouse e così via. Usare queste linee guida per creare esperienze intuitive e distintive ottimizzate per il tocco, ma che funzionano in modo coerente tra i dispositivi di input.
ms.assetid: 1509c885-f4dc-4cf9-86a3-cc6754d3b4a0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 09991d9b1c16c0605c89a695beb14c1117cb54fe8a5de1e2a805f6717070b1d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853280"
---
# <a name="interaction"></a>Interazione

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

L'interazione è la varietà di modi in cui gli utenti interagiscono con l'app, tra cui tocco, tastiera, mouse e così via. Usare queste linee guida per creare esperienze intuitive e distintive ottimizzate per il tocco, ma che funzionano in modo coerente tra i dispositivi di input.

## <a name="design-for-a-touch-first-experience"></a>Progettare per un'esperienza touch-first

Prima di tutto, progetta la tua app partendo dal presupposto che il principale strumento di input usato dagli utenti sarà il tocco. Se si usano i controlli della piattaforma, il supporto per touchpad, mouse e penna/stilo non richiede alcuna programmazione aggiuntiva, perché Windows offre questo supporto gratuitamente.

Tieni presente, tuttavia, che l'interfaccia utente ottimizzata per il tocco non sempre è migliore rispetto a un'interfaccia tradizionale. Entrambi offrono vantaggi e svantaggi specifici della tecnologia e dell'applicazione. Quando si passa a un'interfaccia utente touch-first, è importante comprendere le differenze principali tra tocco (incluso il touchpad), penna/stilo, mouse e input da tastiera. Non dare per scontato le proprietà e i comportamenti familiari del dispositivo di input, perché il tocco Windows 8 non si limita a emulare tale funzionalità.

Come si scoprirà a breve, l'input tocco richiede un approccio diverso alla progettazione dell'interfaccia utente.

**Confrontare i requisiti delle interazioni tramite tocco**

Questa tabella illustra alcune delle differenze tra i dispositivi di input da considerare quando si progettano app dello Store ottimizzate per il tocco Windows touch.



| Fattore          | Interazioni tramite tocco   | Interazioni tramite mouse, tastiera, penna/stilo | Touchpad  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Precisione**<br/>        | L'area di contatto della punta di un dito è di dimensioni maggiori rispetto a una singola coordinata x-y e questo aumenta la probabilità dell'attivazione involontaria di comandi.<br/>                                                               | Il mouse e la penna o lo stilo forniscono una coordinata x-y precisa.<br/>                                                                                                                                                                                                                                            | Uguale al mouse.<br/>                           |
|                                 | La forma dell'area di contatto cambia durante il movimento. <br/>                                                                                                                                       | I movimenti del mouse e i tratti della penna/stilo forniscono coordinate x-y precise. Lo stato attivo della tastiera è esplicito.<br/>                                                                                                                                                                                                   | Uguale al mouse.<br/>                           |
|                                 | Non è presente il cursore del mouse per agevolare la selezione della destinazione.<br/>                                                                                                                                                    | Il cursore del mouse, il cursore della penna/stilo e lo stato attivo della tastiera agevolano la selezione della destinazione.<br/>                                                                                                                                                                                                                   | Uguale al mouse.<br/>                           |
| **Anatomia umana**<br/>    | I movimenti effettuati con la punta delle dita non sono precisi, dato che imprimere a uno o più dita un movimento rettilineo è piuttosto difficile Questo è dovuto alla curvatura delle giunture della mano e al gran numero di giunture coinvolte nel movimento.<br/> | Eseguire un movimento rettilineo con il mouse o con la penna/stilo è più semplice, perché la mano che li controlla percorre una distanza fisica più breve rispetto al cursore sullo schermo.<br/>                                                                                                                    | Uguale al mouse.<br/>                           |
|                                 | Alcune aree della superficie di tocco di un dispositivo di visualizzazione possono essere difficili da raggiungere, a causa della posizione delle dita e della presa dell'utente sul dispositivo.<br/>                                                                | Il mouse e la penna/stilo possono raggiungere qualsiasi parte dello schermo, mentre dovrebbe essere possibile accedere a qualsiasi controllo tramite la tastiera attraverso l'ordine di tabulazione. <br/>                                                                                                                                                                 | Posizione delle dita e presa possono dare qualche problema.<br/> |
|                                 | Gli oggetti possono essere nascosti da una o più dita o dalla mano dell'utente. Questa situazione è nota come occlusione.<br/>                                                                                                   | I dispositivi di input indiretto non provocano fenomeni di occlusione.<br/>                                                                                                                                                                                                                                                       | Uguale al mouse.<br/>                           |
| **Stato oggetto**<br/>     | Il tocco usa un modello basato su due stati: la superficie di tocco di un dispositivo di visualizzazione è stata toccata (on) o non è stata toccata (off). Non esiste uno stato di passaggio del mouse che possa attivare un feedback visivo aggiuntivo.<br/>                         | Mouse, penna/stilo e tastiera espongono un modello basato su tre stati: su (off), giù (on) e passaggio (stato attivo).<br/> Il passaggio consente agli utenti di esplorare e imparare attraverso le descrizioni comandi associate agli elementi dell'interfaccia utente. Gli effetti associati al passaggio e all'impostazione dello stato attivo possono comunicare quali sono gli oggetti interattivi e agevolare la selezione della destinazione. <br/> | Uguale al mouse.<br/>                           |
| **Interazione avanzata**<br/> | Supporto del multitocco: più punti di input (dita) su una superficie di tocco.<br/>                                                                                                                          | Supporta un unico punto di input.<br/>                                                                                                                                                                                                                                                                       | Uguale al tocco.<br/>                           |
|                                 | Supporto della manipolazione diretta di oggetti tramite gesti, ad esempio tocco, trascinamento, scorrimento, avvicinamento delle dita e rotazione.<br/>                                                                                  | Nessun supporto per la manipolazione diretta, perché mouse, penna/stilo e tastiera sono dispositivi di input indiretto.<br/>                                                                                                                                                                                                    | Uguale al mouse.<br/>                           |



 

**Nota**

L'input indiretto ha alle spalle più di 25 anni di perfezionamento. Funzionalità come le descrizioni comandi attivate al passaggio sono state progettate specificamente per l'esplorazione dell'interfaccia utente tramite touchpad, mouse, penna/stilo e tastiera. Funzionalità dell'interfaccia utente simili sono state riprogettate per l'esperienza completa fornita dall'input tramite tocco, senza compromettere l'esperienza utente per questi altri dispositivi.

In questo argomento vengono fornite alcune linee guida generali per l'interazione dell'utente e vengono illustrate le linee guida specifiche del dispositivo.

-   [Tocco](/windows/desktop/uxguide/inter-touch)
-   [Mouse](/windows/desktop/uxguide/inter-mouse)
-   [Penna](/windows/desktop/uxguide/inter-pen)
-   [Tastiera](/windows/desktop/uxguide/inter-keyboard)
-   [Accessibilità](/windows/desktop/uxguide/inter-accessibility)

## <a name="visuals-for-feedback"></a>Oggetti visivi per commenti e suggerimenti

Il feedback visivo appropriato durante le interazioni con l'app consente agli utenti di riconoscere, apprendere e adattarsi al modo in cui le interazioni vengono interpretate dall'app e dal feedback visivo di Windows può indicare interazioni riuscite, stato del sistema di inoltro, migliorare il senso di controllo, ridurre gli errori, aiutare gli utenti a comprendere il sistema e il dispositivo di input e favorire l'interazione.

Il feedback visivo è essenziale quando l'utente si affida all'input tocco per attività che richiedono accuratezza e precisione in base alla posizione. Visualizza il feedback visivo ogni volta che viene rilevato un input tocco per aiutare l'utente a comprendere le eventuali regole di selezione della destinazione personalizzate definite dall'app e dai controlli.

## <a name="optimize-for-accuracy"></a>Ottimizzare per l'accuratezza

L'input tocco include l'intera area di contatto del dito. Questa geometria di contatto viene usata per determinare l'oggetto di destinazione più probabile. Ridimensionare i controlli per garantire un'interfaccia utente comoda con oggetti e controlli facili e sicuri da usare come destinazione.

Dimensioni, spazio e posizione dei controlli per eliminare l'occlusione di dita e mano, in cui l'interfaccia utente viene nascosta dall'interazione dell'utente stessa.

Posiziona i menu, i popup e le descrizioni comando sopra l'area dei contatti, quando possibile.

## <a name="constrain-for-confidence"></a>Vincolare l'attendibilità

Evitare o ridurre al minimo le interazioni con sloppy usando vincoli dell'interfaccia utente.

-   I punti di ancoraggio possono semplificare l'arresto nelle posizioni desiderate. I punti di ancoraggio specificano gli arresti logici nel contenuto dell'app. Dal punto di vista cognitivo, i punti di ancoraggio fungono da meccanismo di paging per l'utente e riducono al minimo l'affaticamento dovuto a scorrimento eccessivo, scorrimento o rotazione. Con essi, è possibile gestire l'input utente impreciso e assicurarsi che sia visualizzato un subset specifico di informazioni sul contenuto o sulla chiave.
-   "guide" direzionali che evidenziano l'asse del movimento (verticale o orizzontale).

## <a name="avoid-timed-interactions"></a>Evitare interazioni a tempo

Le interazioni non devono distinguersi in base al tempo. La stessa interazione deve produrre il medesimo risultato indipendentemente dal tempo impiegato per eseguirla. Le interazioni basate sul tempo introducono ritardi obbligatori per gli utenti e incidono negativamente sia sulla natura coinvolgente della manipolazione diretta che sulla percezione della velocità di risposta del sistema.

Per determinare il comando da eseguire le interazioni a tempo dipendono in genere da soglie invisibili, come tempo, distanza o velocità. Le interazioni programmate non hanno alcun feedback visivo fino a quando il sistema non esegue l'azione e gli utenti devono raggiungere soglie arbitrarie e invisibili per ottenere un risultato. Il feedback visivo immediato durante le interazioni fa sentire l'utente più coinvolto e sicuro e gli dà la sensazione di avere la situazione sotto controllo.

Le interazioni che influiscono direttamente sugli oggetti e simulano interazioni del mondo reale sono più intuitive e individuabili, restano più impresse nella memoria e non si basano su interazioni oscure o astratte.

**Nota:** Un'eccezione a questo è il caso in cui si usano interazioni a tempo specifiche per facilitare l'apprendimento e l'esplorazione (ad esempio, premere e tenere premuto). L'uso di descrizioni e segnali visivi appropriati ha un grande effetto sull'uso delle interazioni avanzate.

