---
title: Esempio di grafica semplice
description: Esempio di grafica semplice
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Windows Media Player, file art
- skins, file art
- file per le interfaccia, grafica
- file di grafica per le interfaccia, esempi
- Windows Media Player, esempi
- skins,examples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbd50cb4ad0dbd76babd99439a885f9e77557d04e18f2698bb970effa23d6b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615947"
---
# <a name="simple-art-example"></a>Esempio di grafica semplice

Sono necessari tre file di grafica per creare un'interfaccia semplice con due pulsanti. Sono necessarie un'immagine primaria e un'immagine di mapping e un'immagine alternativa fornisce un segnale visivo all'utente che è possibile fare clic su un pulsante.

Questi file di grafica sono stati creati in un programma di grafica che usa livelli. L'uso dei livelli rende più semplice assicurarsi che le immagini primarie, di mapping e alternative siano tutte delle stesse dimensioni e allineate tra loro.

Le istruzioni dettagliate sulla creazione dell'immagine sono disponibili nella [Guida alla creazione dell'interfaccia .](skin-creation-guide.md)

## <a name="primary-image"></a>Immagine primaria

L'immagine principale è un semplice ovale giallo con due pulsanti, uno rosa per Windows Media Player e un pulsante viola per arrestarlo. Lo sfondo è leggermente giallo scuro rispetto all'ovale. Questa immagine è illustrata nella figura seguente.

![immagine primaria](images/absam01b.png)

L'immagine principale è stata dalle immagini seguenti, ognuna in un livello separato. Prima di tutto è stato creato un ovale con una smussatura e un effetto rilievo del livello. Questa immagine è illustrata nella figura seguente.

![immagine oval](images/absam01s.png)

Sono stati quindi creati i due pulsanti, con effetti smussatura e rilievo del livello. Questo aspetto è illustrato nella figura seguente.

![due pulsanti](images/absam01p.png)

Successivamente è stato creato lo sfondo dell'immagine. È stato scelto un giallo leggermente più scuro in modo che qualsiasi anti-aliasing tra l'ovale e lo sfondo non verrà notato. Il valore del colore \# è CCCC00. Questa immagine è illustrata nella figura seguente.

![immagine di sfondo](images/absam01y.png)

I livelli che contenevano queste immagini sono stati resi visibili e salvati come copia in formato bitmap, creando l'immagine primaria. L'immagine composita primaria verrà usata **dall'attributo backgroundImage** dell'elemento **VIEW.**

## <a name="mapping-image"></a>Immagine di mapping

È necessaria un'immagine di mapping per specificare quando e dove viene fatto clic su un'interfaccia. È stata creata un'immagine di mapping con un'area rossa e un'area verde. Questa immagine è illustrata nella figura seguente.

![immagine di mapping](images/absam01m.png)

L'area verde verrà usata per identificare l'area sull'interfaccia che inizierà Windows Media Player e l'area rossa verrà usata per arrestarla. L'immagine di mapping ha le stesse dimensioni dell'immagine primaria.

L'immagine di mapping è stata creata copiando il livello pulsante in un nuovo livello e disattivando l'effetto smussatura e rilievo. Le immagini flat sono necessarie per il mapping perché Windows Media Player ricerca di valori di colore singolo in ogni area. Può cercare solo un colore definito dall'utente, ad esempio rosso ( \# FF0000). Se l'immagine ha una smussatura o un altro effetto, non tutto sarà il rosso esatto necessario.

Per rendere i pulsanti di mapping un colore facile da ricordare, le immagini sono state riempite con rosso puro e verde puro, ma è possibile usare qualsiasi colore. È necessario ricordare i numeri di colore nella mappa in modo che possano essere immessi nel file di definizione dell'interfaccia XML. In questo caso, il rosso \# è FF0000 e il verde \# è 00FF00.

Quindi, con solo il nuovo livello visibile, l'immagine è stata salvata come copia in un file BMP. Verrà chiamato dall'attributo **mappingImage** **dell'elemento BUTTONGROUP.**

## <a name="alternate-image"></a>Immagine alternativa

Le immagini alternative non sono necessarie, ma sono molto utili per fornire segnali visivi all'utente. In questo caso, è consigliabile un'immagine al passaggio del mouse in modo che l'utente sappia su quali aree è possibile fare clic.

È stata creata un'immagine alternativa con due pulsanti gialli. Questo aspetto è illustrato nella figura seguente.

![immagine al passaggio del mouse](images/absam01h.png)

L'immagine alternativa è stata creata copiando il livello del pulsante originale in un nuovo livello e quindi modificando il colore di riempimento in giallo. L'effetto smussato e rilievo è stato mantenuto. È stato quindi creato un nuovo livello e sono state aggiunte immagini: la freccia indica "play" e il quadrato indica "stop". Quindi, con solo il nuovo pulsante giallo e i livelli di tipo visibili, l'immagine è stata salvata come copia in un file bitmap.

Il risultato è che quando il puntatore del mouse passa su un'area definita dall'immagine di mapping, viene visualizzata l'immagine al passaggio del mouse, avvisando il lettore che, se fa clic su tale punto, può riprodurre o arrestare il Windows Media Player.

## <a name="final-image"></a>Immagine finale

Ecco l'immagine finale dell'interfaccia.

![immagine finale](images/absam01f.png)

Questa è l'immagine che verrà visualizzata se si passa il mouse sul pulsante rosa a destra.

![passare il puntatore del mouse sul pulsante destro](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>Codice XML per l'esempio di grafica

I dettagli su come scrivere codice [](skin-creation-guide.md)XML sono disponibili nella Guida alla creazione dell'interfaccia, ma per mostrare la piccola parte di codice necessaria per creare un'interfaccia funzionante, ecco il codice per la grafica in questo esempio.

I pulsanti predefiniti vengono usati per le funzioni di riproduzione e arresto. È necessario caricare un file o una playlist dal Windows ancoraggio multimediale. Quando Windows Media Player cambia in modalità interfaccia, viene visualizzata una piccola casella nell'angolo inferiore destro dello schermo. Questa casella è denominata "ancoraggio". Fare clic sull'ancoraggio per ottenere le funzionalità minime necessarie, nel caso in cui un'interfaccia non fornirà un modo per tornare alla modalità completa di Windows Media Player. L'utente può passare da una modalità all'altra usando il menu **Visualizza** in modalità completa oppure facendo clic sull'ancoraggio in modalità interfaccia.


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di grafica**](art-files.md)
</dt> </dl>

 

 




