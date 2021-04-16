---
title: Frame della finestra
description: La maggior parte dei programmi deve usare frame della finestra standard. Le applicazioni immersive possono avere una modalità schermo intero che nasconde la cornice della finestra. Prendere in considerazione l'uso di Glass in modo strategico per un aspetto più semplice, più chiaro e coeso.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104570969"
---
# <a name="window-frames"></a>Frame della finestra

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

La maggior parte dei programmi deve usare frame della finestra standard. Le applicazioni immersive possono avere una modalità schermo intero che nasconde la cornice della finestra. Prendere in considerazione l'uso di Glass in modo strategico per un aspetto più semplice, più chiaro e coeso.

Con una cornice della finestra, gli utenti possono modificare una finestra e visualizzare il titolo e l'icona per identificarne il contenuto.

![screenshot della cornice della finestra intorno alla finestra del blocco note ](images/win-window-frames-image1.png)

Una cornice di finestra tipica.

**Nota:** Le linee guida relative alla gestione e alla [personalizzazione](exper-branding.md) [delle finestre](win-window-mgt.md) sono presentate in articoli distinti.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="glass-window-frames"></a>Cornice della finestra Glass

I frame della finestra vetrata sono un nuovo aspetto interessante di Microsoft Windows estetico, che punta a essere sia accattivante che leggero. Questi frame traslucidi offrono a Windows un aspetto aperto, meno intrusivo, che consente agli utenti di concentrarsi sui contenuti e sulle funzionalità anziché sull'interfaccia che la circonda.

![screenshot della cornice di vetro intorno al calcolatore ](images/win-window-frames-image2.png)

Frame della finestra di vetro.

È possibile usare il vetro in modo strategico in aree piccole all'interno di una finestra che tocca la cornice della finestra. Tali aree sembrano essere parte della cornice della finestra, anche se tecnicamente fanno parte dell'area client della finestra.

![screenshot della finestra con bordo traslucido ](images/win-window-frames-image3.png)

In questo esempio, il vetro viene usato nell'area client per renderlo simile a parte del frame.

### <a name="hidden-frames"></a>Frame nascosti

In alcuni casi la cornice migliore della finestra non è un frame. Questo è spesso il caso della [finestra principale](glossary.md) di applicazioni a [schermo intero](glossary.md) immersive che non vengono usate insieme ad altri programmi, ad esempio lettori multimediali, giochi e applicazioni chiosco.

I visualizzatori di contenuto spesso traggono vantaggio dalla possibilità di visualizzare il contenuto a schermo intero. Gli esempi includono Windows Internet Explorer, raccolta foto di Windows Live, Windows Movie Maker HD, Microsoft PowerPoint e Microsoft Word.

![Screenshot di Media Player nella visualizzazione a schermo intero ](images/win-window-frames-image4.png)

In questo esempio, Windows Media Player può visualizzare il relativo contenuto a schermo intero.

### <a name="custom-frames"></a>Frame personalizzati

La maggior parte delle applicazioni Windows deve usare i frame della finestra standard. Tuttavia, per le applicazioni autonome immersive a schermo intero, ad esempio giochi e applicazioni chiosco, potrebbe essere opportuno usare frame personalizzati per qualsiasi finestra che non viene visualizzata a schermo intero. La motivazione a usare i frame personalizzati dovrebbe essere quella di offrire un'esperienza complessiva univoca, non solo per la [personalizzazione](exper-branding.md).

![illustrazione del puzzle e del frame per immagini strapazzate ](images/win-window-frames-image5.png)

I frame personalizzati sono appropriati per le applicazioni autonome immersive, a schermo intero, ad esempio i giochi.

## <a name="guidelines"></a>Indicazioni

### <a name="window-frames"></a>Frame della finestra

-   Usare i frame della finestra standard.
    -   **Eccezione:** Per offrire alle applicazioni autonome a schermo intero un'unica sensazione:
        -   Prendere in considerazione la possibilità di nascondere la cornice della finestra [principale](glossary.md).
        -   Si consiglia di utilizzare frame personalizzati per la [finestra secondaria](glossary.md).
        -   Se un frame personalizzato è appropriato, scegliere una progettazione leggera e non attirare eccessiva attenzione su se stessa.

            **Non corretto:**

            ![cattura di schermata del frame di distrazione ](images/win-window-frames-image6.png)

            In questo esempio il frame personalizzato disegna troppo attenzione per se stesso.
-   Non aggiungere controlli a una cornice della finestra. In alternativa, inserire i controlli all'interno della finestra.

    **Non corretto:**

    ![screenshot del controllo nella cornice della finestra ](images/win-window-frames-image7.png)

    **Corretto:**

    ![screenshot del controllo nell'area client ](images/win-window-frames-image8.png)

    Nell'esempio corretto, il controllo si trova all'interno dell'area client anziché della cornice della finestra.

### <a name="full-screen-mode"></a>Modalità schermo intero

-   Per i programmi che dispongono di una modalità schermo intero facoltativa, per abilitare la modalità schermo intero:
    -   Disporre di un comando modale a schermo intero sulla barra dei menu o sulla barra degli strumenti. Quando l'utente fa clic sul comando, Mostra il comando nello stato selezionato.

        ![screenshot della finestra con la voce di menu a schermo intero ](images/win-window-frames-image9.png)

        Questo esempio mostra il comando schermo intero insieme al relativo tasto di scelta rapida standard.

-   Utilizzare F11 per il tasto di scelta rapida schermo intero.
-   Se è presente una barra degli strumenti e la modalità schermo intero viene comunemente usata, avere anche un pulsante della barra degli strumenti grafico con una descrizione comando a schermo intero.

    ![screenshot dei pulsanti a schermo intero e di ripristino ](images/win-window-frames-image10.png)

    Esempi di pulsanti della barra degli strumenti a schermo intero.

-   Per eseguire il ripristino dalla modalità schermo intero:
    -   Disporre di un comando modale a schermo intero sulla barra dei menu o sulla barra degli strumenti. Quando l'utente fa clic sul comando, Visualizza il comando nello stato cancellato.
    -   Utilizzare F11 per il tasto di scelta rapida schermo intero. Se non è già assegnato, è possibile usare ESC anche per questo scopo.

### <a name="glass"></a>Vetro

I frame della finestra standard utilizzano automaticamente il vetro in Windows, ma è anche possibile utilizzare il vetro in aree che toccano la cornice della finestra.

-   **Si consiglia di usare il vetro in modo strategico in aree di piccole dimensioni toccando la cornice della finestra senza testo.** Questa operazione può offrire a un programma un aspetto più semplice, più chiaro e più coeso, facendo in modo che l'area appaia come parte del frame.
-   ![screenshot della finestra con bordo traslucido ](images/win-window-frames-image3.png)
-   In questo esempio, Glass concentra l'attenzione dell'utente sul contenuto anziché sui controlli.
-   **Non usare il vetro in situazioni in cui uno sfondo normale della finestra sarebbe più interessante o più semplice da usare.**

**Corretto:**

![screenshot della finestra con quattro elementi grafici ed etichetta ](images/win-window-frames-image11.png)

In questo esempio, Glass viene usato per assegnare alla finestra Alt + Tab un aspetto leggero. Il vetro funziona per questa finestra perché è costituito da grafica e da un'unica etichetta con testo sicuro.

**Non corretto:**

![screenshot della finestra con dodici elementi grafici ](images/win-window-frames-image12.png)

In questo esempio non corretto, l'uso di Glass sta distraendo. Una semplice sfondo della finestra sarebbe una scelta migliore.

 

 