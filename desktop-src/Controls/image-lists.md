---
title: Informazioni sugli elenchi di immagini
description: Un elenco di immagini è una raccolta di immagini delle stesse dimensioni, ognuna delle quali può essere indicata dal relativo indice.
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfbb55ecd972e7f7e257eebabdb94ee40846a4f1b70b2a725ae1b67c6e69e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672207"
---
# <a name="about-image-lists"></a>Informazioni sugli elenchi di immagini

Un elenco di immagini è una raccolta di immagini delle stesse dimensioni, ognuna delle quali può essere indicata dal relativo indice. Gli elenchi di immagini vengono usati per gestire in modo efficiente grandi set di icone o bitmap. Tutte le immagini in un elenco di immagini sono contenute in una singola bitmap ampia in formato dispositivo schermo. Un elenco di immagini può anche includere una bitmap monocromatica che contiene maschere usate per disegnare immagini in modo trasparente (stile icona).

L'API Microsoft Win32 offre funzioni e macro per l'elenco di immagini che consentono di creare ed eliminare elenchi di immagini, aggiungere e rimuovere immagini, sostituire e unire immagini, disegnare immagini e trascinare immagini. Per usare le funzioni dell'elenco di immagini, includere il file di intestazione del controllo comune nei file di codice sorgente e collegarsi alla libreria di esportazione dei controlli comune. Inoltre, prima di chiamare qualsiasi funzione dell'elenco di immagini, usare la [**funzione InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) per assicurarsi che venga caricata la DLL del controllo comune.

In questa sezione vengono trattati gli argomenti seguenti:

-   [Tipi](#types)
-   [Creazione ed eliminazione di elenchi di immagini](#creating-and-destroying-image-lists)
-   [Aggiunta e rimozione di immagini](#adding-and-removing-images)
-   [Sostituzione e unione di immagini](#replacing-and-merging-images)
-   [Disegno di immagini](#drawing-images)
-   [Trascinamento delle immagini](#dragging-images)
-   [Informazioni sull'immagine](#image-information)
-   [Sovrapposizioni di immagini](#image-overlays)
-   [Icone antialias a 32 bit](#32-bit-antialiased-icons)

## <a name="types"></a>Tipi

Esistono due tipi di elenchi di immagini: non mascherati e mascherati. Un elenco di immagini non mascherate è costituito da una bitmap a colori che contiene una o più immagini. Un elenco di immagini mascherate è costituito da due bitmap di dimensioni uguali. La prima è una bitmap a colori che contiene le immagini e la seconda è una bitmap monocromatica che contiene una serie di maschere, una per ogni immagine nella prima bitmap.

Quando un'immagine non mascherata viene disegnata, viene semplicemente copiata nel contesto di dispositivo di destinazione. in altri, viene disegnata sul colore di sfondo esistente del contesto di dispositivo. Quando viene disegnata un'immagine mascherata, i bit dell'immagine vengono combinati con i bit della maschera, producendo in genere aree trasparenti nella bitmap in cui viene visualizzato il colore di sfondo del contesto di dispositivo di destinazione. Esistono diversi stili di disegno che è possibile specificare quando si disegna un'immagine mascherata. Ad esempio, è possibile specificare che l'immagine deve essere dithering per indicare un oggetto selezionato.

## <a name="creating-and-destroying-image-lists"></a>Creazione ed eliminazione di elenchi di immagini

Per creare un elenco di immagini, chiamare la [**funzione ImageList \_ Create.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) I parametri includono il tipo di elenco di immagini da creare, le dimensioni di ogni immagine e il numero di immagini che si intende aggiungere all'elenco. Per un elenco di immagini non mascherate, la funzione crea una singola bitmap sufficientemente grande da contenere il numero specificato di immagini delle dimensioni specificate. Crea quindi un contesto di dispositivo compatibile con lo schermo e seleziona la bitmap al suo interno. Per un elenco di immagini mascherate, la funzione crea due bitmap e due contesti di dispositivo compatibili con lo schermo. Seleziona la bitmap dell'immagine in un contesto di dispositivo e la bitmap della maschera nell'altro. La DLL di controllo comune contiene il codice eseguibile per le funzioni dell'elenco di immagini.

In [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)specificare il numero iniziale di immagini che saranno presenti in un elenco di immagini e il numero di immagini in base al quale l'elenco può aumentare. Pertanto, se si tenta di aggiungere più immagini di quelle specificate inizialmente, l'elenco di immagini aumenta automaticamente per adattarsi alle nuove immagini.

Se [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) ha esito positivo, restituisce un handle per il tipo HIMAGELIST. Questo handle viene utilizzato in altre funzioni dell'elenco di immagini per accedere all'elenco di immagini e gestire le immagini. È possibile aggiungere e rimuovere immagini, copiare immagini da un elenco di immagini a un altro e unire immagini da due elenchi di immagini diversi. Quando non è più necessario un elenco di immagini, è possibile eliminarlo specificandone l'handle in una chiamata alla [**funzione Destroy di ImageList. \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy)

## <a name="adding-and-removing-images"></a>Aggiunta e rimozione di immagini

È possibile aggiungere immagini bitmap, icone o cursori a un elenco di immagini. È possibile aggiungere immagini bitmap specificando gli handle a due bitmap in una chiamata alla [**funzione ImageList \_ Add.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) La prima bitmap contiene una o più immagini da aggiungere alla bitmap dell'immagine e la seconda contiene le maschere da aggiungere alla bitmap della maschera. Per gli elenchi di immagini non mascherate, il secondo handle bitmap viene ignorato. può essere impostato su **NULL.**

La [**funzione ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) aggiunge anche immagini bitmap a un elenco di immagini mascherate. Questa funzione è simile a [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), ad eccezione del fatto che non si specifica una bitmap della maschera. Si specifica invece un colore combinato dal sistema con la bitmap dell'immagine per generare automaticamente le maschere. Ogni pixel del colore specificato nella bitmap dell'immagine viene modificato in nero e il bit corrispondente nella maschera viene impostato su 1. Di conseguenza, qualsiasi pixel nell'immagine corrispondente al colore specificato è trasparente quando viene disegnata l'immagine.

La macro [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) aggiunge un'icona o un cursore a un elenco di immagini. Se l'elenco di immagini è mascherato, **ImageList \_ AddIcon** aggiunge la maschera fornita con l'icona o il cursore alla bitmap della maschera. Se l'elenco di immagini non è mascherato, la maschera per l'icona o il cursore non viene usata durante il disegno dell'immagine.

È possibile creare un'icona basata su un'immagine e una maschera in un elenco di immagini usando la [**funzione ImageList \_ GetIcon.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) La funzione restituisce l'handle per la nuova icona.

[**ImageList \_ Aggiungere**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)e [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) assegnare un indice a ogni immagine quando viene aggiunta a un elenco di immagini. Gli indici sono in base zero. in altri, la prima immagine nell'elenco ha un indice pari a zero, la successiva ha un indice pari a uno e così via. Dopo aver aggiunto una singola immagine, le funzioni restituiscono l'indice dell'immagine. Quando vengono aggiunte più immagini alla volta, le funzioni restituiscono l'indice della prima immagine.

La [**funzione Remove \_ di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) rimuove un'immagine da un elenco di immagini.

## <a name="replacing-and-merging-images"></a>Sostituzione e unione di immagini

Le [**funzioni ImageList \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace) e [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) sostituiscono un'immagine in un elenco di immagini con una nuova immagine. **ImageList \_ Replace** sostituisce un'immagine con un'immagine bitmap e una maschera e **ImageList \_ ReplaceIcon** sostituisce un'immagine con un'icona o un cursore.

La [**funzione ImageList \_ Merge**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge) unisce due immagini, archiviando la nuova immagine in un nuovo elenco di immagini. La nuova immagine viene creata disegnando la seconda immagine in modo trasparente sulla prima. La maschera per la nuova immagine è il risultato dell'esecuzione di un'operazione **OR** logica sui bit delle maschere per le due immagini esistenti.

## <a name="drawing-images"></a>Disegno di immagini

Per disegnare un'immagine, usare la [**funzione ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) Specificare l'handle per un elenco di immagini, l'indice dell'immagine da disegnare, l'handle per il contesto di dispositivo di destinazione, una posizione all'interno del contesto di dispositivo e uno o più stili di disegno.

Quando si specifica lo stile **ILD \_ TRANSPARENT,** [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) usa un processo in due passaggi per disegnare un'immagine mascherata. In primo luogo, esegue **un'operazione and** logica sui bit dell'immagine e sui bit della maschera. Esegue quindi **un'operazione XOR** logica sui risultati della prima operazione e sui bit in background del contesto di dispositivo di destinazione. Questo processo consente di creare aree trasparenti nell'immagine risultante; ovvero ogni bit bianco nella maschera rende trasparente il bit corrispondente nell'immagine.

Prima di disegnare un'immagine mascherata su uno sfondo a tinta unita, è consigliabile usare la funzione [**ImageList \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) per impostare il colore di sfondo dell'elenco immagini sullo stesso colore della destinazione. L'impostazione del colore elimina la necessità di creare aree trasparenti nell'immagine e consente a [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) di copiare semplicemente l'immagine nel contesto di dispositivo di destinazione, con conseguente aumento significativo delle prestazioni. Per disegnare l'immagine, specificare lo stile **ILD \_ NORMAL** in una chiamata a **ImageList \_ Draw** o **ImageList \_ DrawEx**.

È possibile impostare il colore di sfondo per un elenco di immagini mascherate in qualsiasi momento in modo da disegnare correttamente su qualsiasi sfondo a tinta unita. Se si imposta il colore di sfondo su CLR NONE, le immagini vengono disegnate in modo \_ trasparente per impostazione predefinita. Per recuperare il colore di sfondo di un elenco di immagini, usare la [**funzione ImageList \_ GetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor)

Gli **stili ILD \_ BLEND25** e **ILD \_ BLEND50** dithering dell'immagine con il colore di evidenziazione del sistema. Questi stili sono utili se si utilizza un'immagine mascherata per rappresentare un oggetto che l'utente può selezionare. Ad esempio, è possibile usare lo stile **ILD \_ BLEND50** per disegnare l'immagine quando l'utente la seleziona.

Un'immagine non mascherata viene copiata nel contesto di dispositivo di destinazione usando l'operazione raster SRCCOPY. I colori dell'immagine hanno lo stesso aspetto indipendentemente dal colore di sfondo del contesto del dispositivo. Anche gli stili di disegno specificati in [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) non hanno alcun effetto sull'aspetto di un'immagine non mascherata.

## <a name="dragging-images"></a>Trascinamento delle immagini

L'API Win32 include funzioni per trascinare un'immagine sullo schermo. Le funzioni di trascinamento spostano un'immagine in modo uniforme, a colori e senza lampeggiare del cursore. È possibile trascinare immagini mascherate e non mascherate.

La [**funzione ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) avvia un'operazione di trascinamento. I parametri includono l'handle per l'elenco di immagini, l'indice dell'immagine da trascinare e la posizione dell'area sensibile all'interno dell'immagine. L'area sensibile è un singolo pixel che le funzioni di trascinamento riconoscono come posizione esatta dello schermo dell'immagine. In genere, un'applicazione imposta l'area sensibile in modo che coincida con l'area sensibile del cursore del mouse. La [**funzione ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) sposta l'immagine in una nuova posizione.

La [**funzione ImageList \_ DragEnter**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter) imposta la posizione iniziale dell'immagine di trascinamento all'interno di una finestra e disegna l'immagine in corrispondenza della posizione. I parametri includono l'handle per la finestra in cui disegnare l'immagine e le coordinate della posizione iniziale all'interno della finestra. Le coordinate sono relative all'angolo superiore sinistro della finestra, non all'area client. Lo stesso vale per tutte le funzioni di trascinamento delle immagini che accettano le coordinate come parametri. Ciò significa che è necessario compensare la larghezza degli elementi della finestra, ad esempio il bordo, la barra del titolo e la barra dei menu quando si specificano le coordinate. Se si specifica un handle di finestra **NULL** quando si chiama **ImageList \_ DragEnter,** le funzioni di trascinamento disegnano l'immagine nel contesto di dispositivo associato alla finestra desktop e le coordinate sono relative all'angolo superiore sinistro dello schermo.

La [**funzione ImageList \_ SetDragCursorImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) crea una nuova immagine di trascinamento combinando l'immagine specificata (in genere un'immagine del cursore del mouse) con l'immagine di trascinamento corrente. Poiché le funzioni di trascinamento usano la nuova immagine durante un'operazione di trascinamento, è necessario usare la funzione [**ShowCursor**](/windows/desktop/api/winuser/nf-winuser-showcursor) per nascondere il cursore effettivo del mouse dopo aver chiamato **ImageList \_ SetDragCursorImage.** In caso contrario, il sistema potrebbe avere due cursori del mouse per la durata dell'operazione di trascinamento.

Quando un'applicazione chiama [**ImageList \_ BeginDrag,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)il sistema crea un elenco di immagini interno temporaneo e quindi copia l'immagine di trascinamento specificata nell'elenco interno. È possibile recuperare l'handle per l'elenco di immagini di trascinamento temporaneo usando la [**funzione ImageList \_ GetDragImage.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) La funzione recupera anche la posizione di trascinamento corrente e l'offset dell'immagine di trascinamento rispetto alla posizione di trascinamento.

## <a name="image-information"></a>Informazioni sull'immagine

Esistono diverse funzioni che recuperano informazioni da un elenco di immagini. La funzione [**\_ ImageList GetImageInfo**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo) riempie una struttura [**IMAGEINFO**](/windows/desktop/api) con informazioni su una singola immagine, inclusi gli handle delle bitmap dell'immagine e della maschera, il numero di piani colori e bit per pixel e il rettangolo di delimitazione dell'immagine all'interno della bitmap dell'immagine. È possibile usare queste informazioni per modificare direttamente le bitmap per l'immagine. La [**funzione ImageList \_ GetImageCount**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount) recupera il numero di immagini in un elenco di immagini.

## <a name="image-overlays"></a>Sovrimpressione di immagini

Ogni elenco di immagini include un elenco di indici da usare come sovrimpressione. Una sovrimpressione è un'immagine disegnata in modo trasparente su un'altra immagine. Qualsiasi immagine attualmente presente nell'elenco di immagini può essere usata come sovrimpressione. È possibile specificare fino a quattro sovrimpressione per ogni elenco di immagini. Questo limite è stato esteso a 15 nella versione 4.71.

È possibile aggiungere l'indice di un'immagine all'elenco di sovrimpressione usando la funzione [**ImageList \_ SetOverlayImage,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) specificando l'handle per l'elenco di immagini, l'indice dell'immagine esistente e l'indice di sovrimpressione desiderato. Questo, in effetti, indica all'elenco immagini che "l'immagine in corrispondenza dell'indice *x* può essere usata come sovrimpressione e voglio fare riferimento alla sovrimpressione come indice di sovrimpressione *y".* Gli indici di sovrimpressione sono in base uno anziché in base zero perché un indice di sovrimpressione pari a zero indica che non verrà usata alcuna sovrimpressione.

È possibile specificare una sovrimpressione quando si disegna un'immagine con la funzione [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) La sovrimpressione viene specificata eseguendo **un'operazione OR** logica tra i flag di disegno desiderati e il risultato della macro [**INDEXTOOVERLAYMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) La macro **INDEXTOOVERLAYMASK** accetta l'indice di sovrimpressione e lo formatta per l'inclusione con i flag per queste funzioni. Verrà disegnata l'immagine con la sovrimpressione specificata. L'esempio seguente illustra come viene aggiunta e specificata una sovrimpressione quando si disegna l'immagine.


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



Verrà disegnata l'immagine 1 e quindi tale immagine verrà sovrapposta all'immagine 0. Poiché 3 è l'indice di sovrapposizione specificato nella chiamata [**a ImageList \_ SetOverlayImage,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) 3 viene inserito nella macro [**INDEXTOOVERLAYMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask)

## <a name="32-bit-antialiased-icons"></a>Icone antialias a 32 bit

L'antialiasing è una tecnica per attenuare o sfocatura dei bordi acuti. In questo modo le immagini hanno un aspetto più naturale. Gli elenchi di immagini Windows Vista e Windows 7 supportano l'uso di icone e bitmap con antialias a 32 bit. I valori dei colori usano 24 bit e 8 bit vengono usati come canale alfa sulle icone. Per creare un elenco di immagini in grado di gestire un'immagine a 32 bit per pixel (bpp), chiamare la funzione [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) passando un \_ flag ILC COLOR32.

Per creare correttamente icone a 32 bit, è necessario creare più immagini per ogni icona, come illustrato nella figura seguente.

![illustrazione che mostra tre dimensioni di icone per ognuna delle tre profondità dei colori](images/theme2.png)

-   Le prime tre immagini sono in modalità a 16 colori per l'uso in modalità sicura.
-   Le tre icone seguenti vengono usate in modalità a 256 colori.
-   Le ultime tre icone hanno il canale alfa e possono essere usate solo nei sistemi operativi che eseguono colori a 24 bit o versioni successive.
-   L'ordine delle immagini nel formato icona è importante. Se l'ordine è errato, le versioni precedenti Windows funzionano in modo non corretto durante l'estrazione delle icone. L'estrazione non corretta delle icone può causare il danneggiamento della memoria e il rendering non corretto.
-   Le versioni precedenti Windows avevano un limite di risorse di 10 icone.

> [!Note]  
> È possibile usare strumenti di terze parti per generare file icona e bitmap che contengono un canale alfa. Se si usa [**LoadImage per**](/windows/desktop/api/winuser/nf-winuser-loadimagea) caricare una bitmap a 32 bpp che contiene alfa, è necessario specificare il flag LR \_ CREATEDIBSECTION.

 

 

 