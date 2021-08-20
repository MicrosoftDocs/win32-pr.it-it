---
title: Frame di finestra
description: La maggior parte dei programmi deve usare frame di finestra standard. Le applicazioni immersive possono avere una modalità schermo intero che nasconde la cornice della finestra. È consigliabile usare il vetro in modo strategico per un aspetto più semplice, più leggero e coesivo.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dee701f7aad12e348a89034010de1f44134e9d3e
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812260"
---
# <a name="window-frames"></a>Frame di finestra

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

La maggior parte dei programmi deve usare frame di finestra standard. Le applicazioni immersive possono avere una modalità schermo intero che nasconde la cornice della finestra. È consigliabile usare il vetro in modo strategico per un aspetto più semplice, più leggero e coesivo.

Con una cornice di finestra, gli utenti possono modificare una finestra e visualizzare il titolo e l'icona per identificarne il contenuto.

![Screenshot della cornice della finestra intorno alla finestra del Blocco note ](images/win-window-frames-image1.png)

Cornice di finestra tipica.

**Nota:** Le linee guida relative [alla gestione delle finestre](win-window-mgt.md) e alla [personalizzazione](exper-branding.md) sono presentate in articoli separati.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="glass-window-frames"></a>Riquadri della finestra di cristallo

Le finestre in vetro sono un nuovo aspetto straordinario dell'Windows di Microsoft, con l'obiettivo di essere attraenti e leggeri. Questi fotogrammi traslucidi offrono alle finestre un aspetto aperto e meno intrusivo, consentendo agli utenti di concentrarsi sul contenuto e sulle funzionalità anziché sull'interfaccia che la circonda.

![Screenshot della cornice di cristallo intorno alla calcolatrice ](images/win-window-frames-image2.png)

Riquadri della finestra di cristallo.

È possibile usare il vetro in modo strategico in piccole aree all'interno di una finestra che tocca la cornice della finestra. Tali aree sembrano far parte della cornice della finestra, anche se tecnicamente fanno parte dell'area client della finestra.

![Screenshot della finestra con bordo traslucido ](images/win-window-frames-image3.png)

In questo esempio, glass viene usato nell'area client per renderlo simile a una parte del frame.

### <a name="hidden-frames"></a>Frame nascosti

A volte la cornice di finestra migliore non è affatto un frame. Questo è spesso il [](glossary.md) caso della [](glossary.md) finestra principale delle applicazioni immersive a schermo intero che non vengono usate in combinazione con altri programmi, ad esempio lettori multimediali, giochi e applicazioni in modalità tutto schermo.

I visualizzatori di contenuti spesso traggono vantaggio dalla possibilità di visualizzare il contenuto a schermo intero. Ad esempio Windows Internet Explorer, Raccolta foto di Windows Live, Windows Movie Maker HD, Microsoft PowerPoint e Microsoft Word.

![Screenshot del lettore multimediale nella visualizzazione a schermo intero ](images/win-window-frames-image4.png)

In questo esempio, Windows Media Player visualizzare il contenuto a schermo intero.

### <a name="custom-frames"></a>Frame personalizzati

La maggior Windows applicazioni devono usare i frame di finestra standard. Tuttavia, per le applicazioni autonome e immersive a schermo intero, come giochi e applicazioni in modalità tutto schermo, può essere opportuno usare fotogrammi personalizzati per tutte le finestre che non vengono visualizzate a schermo intero. La motivazione all'uso di frame personalizzati deve essere di offrire all'esperienza complessiva un aspetto unico, non solo per [la personalizzazione](exper-branding.md)di .

![illustrazione del rompicapo e della cornice di immagini inesamblate ](images/win-window-frames-image5.png)

I frame personalizzati sono appropriati per applicazioni autonome, ad esempio giochi, a schermo intero e immersive.

## <a name="guidelines"></a>Indicazioni

### <a name="window-frames"></a>Frame di finestra

-   Usare frame di finestra standard.
    -   **Eccezione:** Per offrire un aspetto unico alle applicazioni autonome a schermo intero immersivo:
        -   È consigliabile nascondere la cornice della [finestra primaria.](glossary.md)
        -   Prendere in considerazione l'uso di frame personalizzati per [la finestra secondaria.](glossary.md)
        -   Se un frame personalizzato è appropriato, scegliere una progettazione leggera e non attirare l'attenzione su se stessa.

            **Non corretto:**

            ![Screenshot del frame di distrazione ](images/win-window-frames-image6.png)

            In questo esempio, il frame personalizzato richiama un'attenzione troppo grande su se stesso.
-   Non aggiungere controlli a una cornice della finestra. Inserire invece i controlli all'interno della finestra.

    **Non corretto:**

    ![Screenshot del controllo nella cornice della finestra ](images/win-window-frames-image7.png)

    **Corretto:**

    ![Screenshot del controllo nell'area client ](images/win-window-frames-image8.png)

    Nell'esempio corretto, il controllo si trova all'interno dell'area client anziché della cornice della finestra.

### <a name="full-screen-mode"></a>Modalità schermo intero

-   Per i programmi che hanno una modalità schermo intero facoltativa, per abilitare la modalità schermo intero:
    -   Disporre di un comando modale a schermo intero nella barra dei menu o nella barra degli strumenti. Quando l'utente fa clic sul comando, mostra il comando nello stato selezionato.

        ![Screenshot della finestra con voce di menu a schermo intero ](images/win-window-frames-image9.png)

        Questo esempio mostra il comando a schermo intero insieme al tasto di scelta rapida standard.

-   Usare F11 per il tasto di scelta rapida a schermo intero.
-   Se è presente una barra degli strumenti e viene usata in genere la modalità schermo intero, è anche disponibile un pulsante della barra degli strumenti grafica con una descrizione comando a schermo intero.

    ![Screenshot dei pulsanti a schermo intero e ripristino ](images/win-window-frames-image10.png)

    Esempi di pulsanti della barra degli strumenti a schermo intero.

-   Per ripristinare la modalità schermo intero:
    -   Disporre di un comando modale a schermo intero nella barra dei menu o nella barra degli strumenti. Quando l'utente fa clic sul comando, mostra il comando nello stato deselezionato.
    -   Usare F11 per il tasto di scelta rapida a schermo intero. Se non è già stato assegnato, è anche possibile usare ESC a questo scopo.

### <a name="glass"></a>Vetro

Le finestre standard usano il vetro automaticamente Windows, ma è anche possibile usare il vetro nelle aree che toccano la cornice della finestra.

-   **È consigliabile usare il vetro in modo strategico in aree di piccole dimensioni che toccano la cornice della finestra senza testo.** In questo modo, un programma può avere un aspetto più semplice, più leggero e più coeso facendo sembrare che l'area appaia parte del frame.
-   ![Screenshot della finestra con bordo traslucido ](images/win-window-frames-image3.png)
-   In questo esempio Glass concentra l'attenzione dell'utente sul contenuto anziché sui controlli.
-   **Non usare il vetro in situazioni in cui uno sfondo di una finestra normale sarebbe più interessante o più facile da usare.**

**Corretto:**

![Screenshot della finestra con quattro elementi grafici ed etichetta ](images/win-window-frames-image11.png)

In questo esempio, glass viene usato per assegnare alla finestra ALT+TAB un aspetto leggero. Glass funziona per questa finestra perché è costituito da grafica e una singola etichetta di testo sicuro.

**Non corretto:**

![Screenshot della finestra con dodici elementi grafici ](images/win-window-frames-image12.png)

In questo esempio non corretto, l'uso del vetro distrae. Uno sfondo di finestra normale è una scelta migliore.

 

 
