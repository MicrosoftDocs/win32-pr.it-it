---
title: Esempio di arte semplice
description: Esempio di arte semplice
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, esempi
- Windows Media Player Skin, esempi
- interfacce, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710009"
---
# <a name="simple-art-example"></a>Esempio di arte semplice

Sono necessari tre file di immagine per creare un'interfaccia semplice con due pulsanti. Sono necessarie un'immagine primaria e un'immagine di mapping e un'immagine alternativa fornisce un segnale visivo all'utente che è possibile fare clic su un pulsante.

Questi file di immagine sono stati creati in un programma artistico che usa i livelli. L'uso dei livelli semplifica la verifica dell'uniformità delle dimensioni delle immagini primarie, di mapping e alternative.

Le istruzioni dettagliate sulla creazione dell'arte sono disponibili nella [Guida alla creazione dell'interfaccia](skin-creation-guide.md).

## <a name="primary-image"></a>Immagine primaria

L'immagine principale è un semplice ovale giallo con due pulsanti, uno rosa per avviare Windows Media Player e il pulsante viola per arrestarlo. Lo sfondo è un colore giallo leggermente più scuro rispetto all'ovale. Questa immagine è illustrata nella figura seguente.

![immagine primaria](images/absam01b.png)

L'immagine principale è stata dalle immagini seguenti, ognuna in un livello separato. Prima di tutto è stato creato un Oval con un effetto smussato e rilievo livello. Questa immagine è illustrata nella figura seguente.

![immagine ovale](images/absam01s.png)

Sono stati creati i due pulsanti, anche con effetti smussato e rilievo del livello. Questo aspetto è illustrato nella figura seguente.

![due pulsanti](images/absam01p.png)

Successivamente è stato creato lo sfondo dell'immagine. È stato scelto un giallo leggermente più scuro in modo che non venga notato alcun anti-aliasing tra l'ovale e lo sfondo. Il valore del colore è \# CCCC00. Questa immagine è illustrata nella figura seguente.

![immagine di sfondo](images/absam01y.png)

I livelli che contenevano queste immagini erano resi visibili e salvati come copia in formato bitmap, creando l'immagine principale. L'immagine composita primaria verrà utilizzata dall'attributo **BackgroundImage** dell'elemento **View** .

## <a name="mapping-image"></a>Immagine di mapping

È necessaria un'immagine di mapping per specificare quando e dove viene fatto clic su un'interfaccia. È stata creata un'immagine di mapping con un'area rossa e un'area verde. Questa immagine è illustrata nella figura seguente.

![immagine di mapping](images/absam01m.png)

L'area verde verrà usata per identificare l'area nell'interfaccia che avvierà Windows Media Player e l'area rossa verrà usata per arrestarla. L'immagine di mapping ha le stesse dimensioni dell'immagine principale.

L'immagine di mapping è stata creata copiando il livello del pulsante in un nuovo livello e disattivando l'effetto smussatura e rilievo. Per il mapping sono necessarie immagini flat perché Windows Media Player cercherà i valori a colore singolo in ogni area. Può solo cercare un colore definito, ad esempio rosso ( \# FF0000). Se l'immagine ha una smussatura o un altro effetto, non tutto sarà il rosso esatto necessario.

Per fare in modo che i pulsanti di mapping siano un colore semplice da ricordare, le immagini sono state riempite con il rosso puro e puro verde, ma è possibile usare qualsiasi colore. È necessario ricordare i numeri di colore nella mappa in modo che possano essere immessi nel file di definizione dell'interfaccia XML. In questo caso, il colore rosso è \# ff0000 e verde è \# 00FF00.

Quindi, solo con il nuovo livello visibile, l'immagine è stata salvata come copia in un file BMP. Verrà chiamato dall'attributo **mappingImage** dell'elemento **ButtonGroup** .

## <a name="alternate-image"></a>Immagine alternativa

Le immagini alternative non sono necessarie, ma sono molto utili per fornire segnali visivi all'utente. In questo caso, è consigliabile usare un'immagine del passaggio del mouse in modo che l'utente sappia quali aree possono essere selezionate.

È stata creata un'immagine alternativa con due pulsanti gialli. Questo aspetto è illustrato nella figura seguente.

![immagine del passaggio del mouse](images/absam01h.png)

L'immagine alternativa è stata creata copiando il livello del pulsante originale in un nuovo livello e quindi cambiando il colore di riempimento in giallo. L'effetto smussatura e rilievo è stato mantenuto. È stato creato un nuovo livello e sono state aggiunte le immagini: la freccia indica "Play" e il quadrato indica "Stop". Quindi, con il nuovo pulsante giallo e i livelli di tipo visibili, l'immagine è stata salvata come copia in un file bitmap.

Il risultato è che quando il mouse viene spostato su un'area definita dall'immagine di mapping, viene visualizzata l'immagine del passaggio del mouse, che avvisa il lettore che se fa clic su tale punto, può riprodurre o arrestare Windows Media Player.

## <a name="final-image"></a>Immagine finale

Di seguito è illustrata l'immagine finale dell'interfaccia.

![immagine finale](images/absam01f.png)

Si tratta dell'immagine che verrà visualizzata se si passa il mouse sul pulsante rosa a destra.

![pulsante con il pulsante destro del mouse](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>Codice XML per l'esempio di arte

Di seguito sono riportati i dettagli relativi alla scrittura di codice XML nella [Guida alla creazione dell'interfaccia](skin-creation-guide.md), ma per mostrare la quantità di codice necessaria per creare un'interfaccia di lavoro, ecco il codice per l'artwork in questo esempio.

I pulsanti predefiniti vengono usati per le funzioni play e stop. È necessario caricare un file o una playlist dal Windows Media Anchor. Quando Windows Media Player passa alla modalità Skin, viene visualizzata una piccola casella nell'angolo inferiore destro dello schermo. Questa casella è denominata "ancoraggio". Facendo clic sull'ancoraggio si ottiene la funzionalità minima necessaria, nel caso in cui un'interfaccia non fornisca un modo per tornare alla modalità completa di Windows Media Player. L'utente può passare da una modalità all'altra tramite il menu **Visualizza** se è in modalità completa oppure facendo clic sull'ancoraggio se in modalità interfaccia.


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

[**File di immagine**](art-files.md)
</dt> </dl>

 

 




