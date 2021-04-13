---
title: Informazioni sugli elenchi di immagini
description: Un elenco di immagini è una raccolta di immagini della stessa dimensione, a cui è possibile fare riferimento in base al relativo indice.
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f059e89b04d16088fff1d937bd29cb23a427d4c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339335"
---
# <a name="about-image-lists"></a>Informazioni sugli elenchi di immagini

Un elenco di immagini è una raccolta di immagini della stessa dimensione, a cui è possibile fare riferimento in base al relativo indice. Gli elenchi di immagini vengono utilizzati per gestire in modo efficiente grandi set di icone o bitmap. Tutte le immagini in un elenco di immagini sono contenute in un'unica bitmap a caratteri wide nel formato del dispositivo dello schermo. Un elenco di immagini può includere anche una bitmap monocromatica che contiene le maschere usate per creare le immagini in modo trasparente (stile icona).

L'API Microsoft Win32 fornisce le funzioni e le macro dell'elenco immagini che consentono di creare ed eliminare in modo permanente elenchi di immagini, aggiungere e rimuovere immagini, sostituire e unire immagini, creare immagini e trascinare immagini. Per usare le funzioni dell'elenco immagini, includere il file di intestazione del controllo comune nei file di codice sorgente e creare un collegamento con la libreria di esportazione del controllo comune. Inoltre, prima di chiamare qualsiasi funzione dell'elenco di immagini, usare la funzione [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) per assicurarsi che la dll del controllo comune venga caricata.

In questa sezione vengono trattati gli argomenti seguenti:

-   [Tipi](#types)
-   [Creazione ed eliminazione degli elenchi di immagini](#creating-and-destroying-image-lists)
-   [Aggiunta e rimozione di immagini](#adding-and-removing-images)
-   [Sostituzione e Unione di immagini](#replacing-and-merging-images)
-   [Disegno di immagini](#drawing-images)
-   [Trascinamento di immagini](#dragging-images)
-   [Informazioni immagine](#image-information)
-   [Sovrimpressioni immagini](#image-overlays)
-   [Icone con antialias a 32 bit](#32-bit-antialiased-icons)

## <a name="types"></a>Tipi

Esistono due tipi di elenchi di immagini: non mascherati e mascherati. Un elenco di immagini non mascherato è costituito da una bitmap di colore che contiene una o più immagini. Un elenco di immagini mascherate è costituito da due bitmap di uguale dimensione. Il primo è una mappa di bit di colore che contiene le immagini e la seconda è una bitmap monocromatica che contiene una serie di maschere, una per ogni immagine nella prima bitmap.

Quando viene disegnata un'immagine non mascherata, viene semplicemente copiata nel contesto del dispositivo di destinazione. ovvero viene disegnato sul colore di sfondo esistente del contesto di dispositivo. Quando viene disegnata un'immagine mascherata, i bit dell'immagine vengono combinati con i bit della maschera, in genere producendo aree trasparenti nella bitmap in cui viene visualizzato il colore di sfondo del contesto di dispositivo di destinazione. Sono disponibili diversi stili di disegno che è possibile specificare durante il disegno di un'immagine mascherata. Ad esempio, è possibile specificare che l'immagine deve essere dimostrata per indicare un oggetto selezionato.

## <a name="creating-and-destroying-image-lists"></a>Creazione ed eliminazione degli elenchi di immagini

Per creare un elenco di immagini, chiamare la funzione [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) . I parametri includono il tipo di elenco di immagini da creare, le dimensioni di ogni immagine e il numero di immagini che si desidera aggiungere all'elenco. Per un elenco di immagini non mascherate, la funzione crea una singola bitmap sufficientemente grande da poter conservare il numero specificato di immagini delle dimensioni specificate. Crea quindi un contesto di dispositivo compatibile con la schermata e ne seleziona la bitmap. Per un elenco di immagini mascherate, la funzione crea due bitmap e due contesti di dispositivo compatibili con la schermata. Seleziona la bitmap dell'immagine in un contesto di dispositivo e la bitmap della maschera nell'altra. La DLL del controllo comune contiene il codice eseguibile per le funzioni dell'elenco di immagini.

In [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)specificare il numero iniziale di immagini che saranno presenti in un elenco di immagini, nonché il numero di immagini in base alle quali l'elenco può aumentare. Quindi, se si tenta di aggiungere più immagini rispetto a quanto specificato inizialmente, l'elenco di immagini cresce automaticamente per adattarsi alle nuove immagini.

Se [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) ha esito positivo, restituisce un handle al tipo HIMAGELIST. Usare questo handle in altre funzioni dell'elenco immagini per accedere all'elenco di immagini e gestire le immagini. È possibile aggiungere e rimuovere immagini, copiare immagini da un elenco di immagini a un altro e unire immagini da due elenchi di immagini diversi. Quando un elenco di immagini non è più necessario, è possibile eliminarlo specificando il relativo handle in una chiamata alla funzione di [**\_ eliminazione ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy) .

## <a name="adding-and-removing-images"></a>Aggiunta e rimozione di immagini

È possibile aggiungere immagini bitmap, icone o cursori a un elenco di immagini. Per aggiungere immagini bitmap, è necessario specificare gli handle per due bitmap in una chiamata alla funzione di [**\_ aggiunta ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) . La prima bitmap contiene una o più immagini da aggiungere alla bitmap dell'immagine e la seconda bitmap contiene le maschere da aggiungere alla bitmap della maschera. Per gli elenchi di immagini non mascherate, il secondo handle di bitmap viene ignorato; può essere impostato su **null**.

La [**funzione \_ AddMasked di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) aggiunge anche immagini bitmap a un elenco di immagini mascherate. Questa funzione è simile a [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), ad eccezione del fatto che non si specifica una bitmap mask. Si specifica invece un colore che il sistema combina con la bitmap dell'immagine per generare automaticamente le maschere. Ogni pixel del colore specificato nella bitmap dell'immagine viene modificato in nero e il bit corrispondente nella maschera è impostato su 1. Di conseguenza, qualsiasi pixel nell'immagine che corrisponde al colore specificato è trasparente quando viene disegnata l'immagine.

La [**macro \_ addicon ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) aggiunge un'icona o un cursore a un elenco di immagini. Se l'elenco di immagini è mascherato, **ImageList \_ addicon** aggiunge la maschera fornita con l'icona o il cursore alla bitmap della maschera. Se l'elenco di immagini non è mascherato, la maschera per l'icona o il cursore non viene utilizzata durante il disegno dell'immagine.

È possibile creare un'icona basata su un'immagine e una maschera in un elenco di immagini usando la funzione [**ImageList \_ GetIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) . La funzione restituisce l'handle per l'icona nuova.

[**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)e [**ImageList \_ addicon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) assegnano un indice a ogni immagine quando viene aggiunta a un elenco di immagini. Gli indici sono in base zero; ovvero la prima immagine dell'elenco ha un indice pari a zero, il successivo ha un indice di uno e così via. Dopo l'aggiunta di una singola immagine, le funzioni restituiscono l'indice dell'immagine. Quando viene aggiunta più di un'immagine alla volta, le funzioni restituiscono l'indice della prima immagine.

La funzione di [**\_ rimozione ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) rimuove un'immagine da un elenco di immagini.

## <a name="replacing-and-merging-images"></a>Sostituzione e Unione di immagini

Le funzioni [**ImageList \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace) e [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) sostituiscono un'immagine in un elenco di immagini con una nuova immagine. **ImageList \_ Sostituisci** sostituisce un'immagine con un'immagine bitmap e una maschera e **ImageList \_ ReplaceIcon** sostituisce un'immagine con un'icona o un cursore.

La funzione di [**\_ merge ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge) unisce due immagini, archiviando la nuova immagine in un nuovo elenco di immagini. La nuova immagine viene creata disegnando la seconda immagine in modo trasparente sulla prima. La maschera per la nuova immagine è il risultato dell'esecuzione di un'operazione **or** logica sui bit delle maschere per le due immagini esistenti.

## <a name="drawing-images"></a>Disegno di immagini

Per creare un'immagine, è possibile usare la funzione [**ImageList \_ disegnato**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . È possibile specificare l'handle per un elenco di immagini, l'indice dell'immagine da disegnare, l'handle per il contesto di dispositivo di destinazione, una posizione all'interno del contesto di dispositivo e uno o più stili di disegno.

Quando si specifica lo **stile \_ trasparente ILD** , [**ImageList \_ Disegna**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) usa un processo in due passaggi per creare un'immagine mascherata. Innanzitutto, esegue un'operazione **and** logica sui bit dell'immagine e sui bit della maschera. Esegue quindi un'operazione **Xor** logica sui risultati della prima operazione e sui bit di sfondo del contesto di dispositivo di destinazione. Questo processo consente di creare aree trasparenti nell'immagine risultante; ovvero ogni bit bianco nella maschera rende trasparente il bit corrispondente nell'immagine.

Prima di disegnare un'immagine mascherata su uno sfondo a tinta unita, è necessario usare la funzione [**\_ SetBkColor di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) per impostare il colore di sfondo dell'elenco di immagini sullo stesso colore della destinazione. L'impostazione del colore Elimina la necessità di creare aree trasparenti nell'immagine e consente a [**ImageList \_ disegnato**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) di copiare semplicemente l'immagine nel contesto di dispositivo di destinazione, causando un aumento significativo delle prestazioni. Per creare l'immagine, specificare lo **stile \_ normale ILD** in una chiamata a **ImageList \_ Disegna** o **ImageList \_ DrawEx**.

È possibile impostare il colore di sfondo per un elenco di immagini mascherato in qualsiasi momento, in modo che venga disegnato correttamente in uno sfondo a tinta unita. Se si imposta il colore di sfondo su CLR None, le \_ immagini verranno disegnate in modo trasparente per impostazione predefinita. Per recuperare il colore di sfondo di un elenco di immagini, usare la funzione [**\_ GetBkColor di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor) .

Gli stili **ILD \_ BLEND25** e **ILD \_ BLEND50** dithering l'immagine con il colore di evidenziazione del sistema. Questi stili sono utili se si utilizza un'immagine mascherata per rappresentare un oggetto che l'utente può selezionare. Ad esempio, è possibile usare lo **stile \_ BLEND50 di ILD** per creare l'immagine quando l'utente la seleziona.

Un'immagine non mascherata viene copiata nel contesto di dispositivo di destinazione tramite l'operazione SRCCOPY raster. I colori dell'immagine hanno lo stesso aspetto indipendentemente dal colore di sfondo del contesto del dispositivo. Gli stili di disegno specificati in [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) non hanno effetto anche sull'aspetto di un'immagine non mascherata.

## <a name="dragging-images"></a>Trascinamento di immagini

L'API Win32 include funzioni per il trascinamento di un'immagine sullo schermo. Le funzioni di trascinamento spostano un'immagine in modo uniforme, in colore e senza lampeggiare del cursore. È possibile trascinare le immagini mascherate e non mascherate.

La [**funzione \_ BeginDrag di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) inizia un'operazione di trascinamento. I parametri includono l'handle per l'elenco di immagini, l'indice dell'immagine da trascinare e la posizione dell'area sensibile all'interno dell'immagine. L'area sensibile è un singolo pixel che le funzioni di trascinamento riconoscono come posizione dello schermo esatta dell'immagine. In genere, un'applicazione imposta l'area sensibile in modo che corrisponda all'area sensibile del cursore del mouse. La [**funzione \_ DragMove di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) sposta l'immagine in una nuova posizione.

La funzione [**ImageList \_ DragEnter**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter) imposta la posizione iniziale dell'immagine di trascinamento all'interno di una finestra e disegna l'immagine in corrispondenza della posizione. I parametri includono l'handle per la finestra in cui si desidera creare l'immagine e le coordinate della posizione iniziale all'interno della finestra. Le coordinate sono relative all'angolo superiore sinistro della finestra, non all'area client. Lo stesso vale per tutte le funzioni di trascinamento delle immagini che accettano le coordinate come parametri. Ciò significa che è necessario compensare le larghezze degli elementi della finestra quali il bordo, la barra del titolo e la barra dei menu quando si specificano le coordinate. Se si specifica un handle di finestra **null** quando si chiama **ImageList \_ DragEnter**, le funzioni di trascinamento disegnano l'immagine nel contesto di dispositivo associato alla finestra desktop e le coordinate sono relative all'angolo superiore sinistro dello schermo.

La [**funzione \_ SetDragCursorImage di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) crea una nuova immagine di trascinamento combinando l'immagine specificata, in genere un'immagine del cursore del mouse, con l'immagine di trascinamento corrente. Poiché le funzioni di trascinamento utilizzano la nuova immagine durante un'operazione di trascinamento, è necessario utilizzare la funzione [**ShowCursor**](/windows/desktop/api/winuser/nf-winuser-showcursor) per nascondere il cursore del mouse effettivo dopo la chiamata a **ImageList \_ SetDragCursorImage**. In caso contrario, è possibile che nel sistema siano presenti due cursori del mouse per la durata dell'operazione di trascinamento.

Quando un'applicazione chiama [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag), il sistema crea un elenco di immagini interne temporaneo, quindi copia l'immagine di trascinamento specificata nell'elenco interno. È possibile recuperare l'handle per l'elenco di immagini di trascinamento temporaneo usando la funzione [**\_ GetDragImage di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) . La funzione recupera inoltre la posizione di trascinamento corrente e l'offset dell'immagine di trascinamento rispetto alla posizione di trascinamento.

## <a name="image-information"></a>Informazioni immagine

Sono disponibili numerose funzioni che recuperano informazioni da un elenco di immagini. La [**funzione \_ GetImageInfo di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo) riempie una struttura [**IMAGEINFO**](/windows/desktop/api) con informazioni su una singola immagine, inclusi gli handle delle bitmap di immagine e maschera, il numero di piani di colore e bit per pixel e il rettangolo di delimitazione dell'immagine nella bitmap dell'immagine. È possibile usare queste informazioni per modificare direttamente le bitmap per l'immagine. La [**funzione \_ GetImageCount di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount) Recupera il numero di immagini in un elenco di immagini.

## <a name="image-overlays"></a>Sovrimpressioni immagini

Ogni elenco di immagini include un elenco di indici da utilizzare come sovrimpressioni. Una sovrapposizione è un'immagine disegnata in modo trasparente su un'altra immagine. Tutte le immagini attualmente presenti nell'elenco immagini possono essere utilizzate come sovrimpressione. È possibile specificare fino a quattro sovrapposizioni per ogni elenco di immagini. Questo limite è stato esteso a 15 nella versione 4,71.

È possibile aggiungere l'indice di un'immagine all'elenco di sovrimpressioni utilizzando la funzione [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) , specificando l'handle per l'elenco di immagini, l'indice dell'immagine esistente e l'indice sovrapposto desiderato. Questo, in effetti, indica all'elenco di immagini che "l'immagine in corrispondenza dell'indice *x* può essere usata come sovrapposizione e voglio fare riferimento alla sovrapposizione come indice di sovrapposizione *y*". Gli indici di sovrimpressione sono basati su uno anziché su zero perché un indice sovrapposto pari a zero indica che non verrà usata alcuna sovrimpressione.

È possibile specificare una sovrapposizione quando si disegna un'immagine con la funzione [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . La sovrapposizione viene specificata eseguendo un'operazione **or** logica tra i flag di disegno desiderati e il risultato della macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . La macro **INDEXTOOVERLAYMASK** accetta l'indice overlay e lo formatta per l'inclusione con i flag per queste funzioni. Verrà creata l'immagine con la sovrapposizione specificata. Nell'esempio seguente viene illustrato come una sovrapposizione viene aggiunta e specificata durante il disegno dell'immagine.


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



Verrà creata l'immagine 1 e quindi sovrapposta all'immagine con l'immagine 0. Poiché 3 è l'indice di sovrapposizione specificato nella chiamata [**\_ SetOverlayImage di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) , 3 viene inserito nella macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) .

## <a name="32-bit-antialiased-icons"></a>Icone con antialias a 32 bit

L'anti-aliasing è una tecnica per l'ammorbidimento o la sfocatura di spigoli acuti. In questo modo, le immagini offrono un aspetto più naturale. Gli elenchi di immagini in Windows Vista e Windows 7 supportano l'uso di icone e bitmap con antialias a 32 bit. I valori dei colori utilizzano 24 bit e 8 bit vengono utilizzati come canale alfa sulle icone. Per creare un elenco di immagini in grado di gestire un'immagine di 32 bit per pixel (BPP), chiamare la funzione [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) , passando un \_ flag ILC COLOR32.

Per creare correttamente icone a 32 bit, è necessario creare più immagini per ogni icona, come illustrato nella figura seguente.

![illustrazione che mostra tre dimensioni delle icone per ognuna delle tre profondità dei colori](images/theme2.png)

-   Le prime tre immagini sono in modalità a 16 colori per l'uso in modalità provvisoria.
-   Le tre icone successive vengono usate in modalità colore 256.
-   Le ultime tre icone hanno il canale alfa e possono essere usate solo nei sistemi operativi che eseguono un colore a 24 bit o superiore.
-   L'ordine delle immagini nel formato dell'icona è rilevante. Se l'ordine non è corretto, le versioni precedenti di Windows funzionano male quando si estraggono le icone. L'estrazione errata delle icone può causare il danneggiamento della memoria e il rendering errato.
-   Nelle versioni precedenti di Windows era presente un limite di risorse di 10 icone.

> [!Note]  
> È possibile usare strumenti di terze parti per generare file di icona e bitmap contenenti un canale alfa. Se si usa [**LoadImage**](/windows/desktop/api/winuser/nf-winuser-loadimagea) per caricare una bitmap 32 BPP che contiene Alpha, è necessario specificare il flag LR \_ CREATEDIBSECTION.

 

 

 