---
title: Creazione dell'immagine del passaggio del mouse
description: Creazione dell'immagine del passaggio del mouse
ms.assetid: 169a99ba-96a0-4487-aa1c-07c83c0bc237
keywords:
- creazione di interfacce, immagini hover
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, immagini hover
- Interfacce di Media Player di Windows, immagini del passaggio del mouse
- interfacce, immagini hover
- immagini del passaggio del mouse nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d7f5bbb8b57820c2805b9b9d6ea79762933035
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328511"
---
# <a name="creating-the-hover-image"></a>Creazione dell'immagine del passaggio del mouse

L'immagine principale di questa interfaccia è costituita da due pulsanti che si siedono su un Oval. Per fornire all'utente un'indicazione sulle operazioni da eseguire, è possibile aggiungere immagini hover. Si tratta di immagini alternative visualizzate quando l'utente posiziona il puntatore del mouse su un pulsante. I pulsanti del passaggio del mouse contengono anche i simboli di controllo Play e stop VCR, in modo che gli utenti sappiano esattamente cosa possono fare. L'uso delle immagini hover consente di creare interfacce artistiche complesse, autodocumentate.

Per creare l'immagine del passaggio del mouse, è necessario eseguire i due pulsanti creati per il file dell'immagine principale, copiarli in nuovi livelli e aggiungere altri livelli per il testo. Eseguire la procedura descritta di seguito:

1.  Copiare il livello del pulsante Chiudi e rinominarlo "close hover".
2.  Usare la selezione colori per creare un colore di primo piano di un giallo chiaro ( \# CCFF33). Questo è stato scelto per contrastare i colori dei pulsanti. Usare quindi lo strumento Secchiello per riempire l'interno del cerchio nel livello Close hover.
3.  Copiare il livello del pulsante Play e rinominarlo "Play hover".
4.  Usare lo strumento Secchiello per riempire l'interno del cerchio nel livello Play hover con lo stesso colore del cerchio close hover.
5.  Creare un nuovo livello e denominarlo "close Square". Usare la selezione colori per creare un colore di primo piano di blu scuro. Usare lo strumento penna per tracciare un quadrato, trasformarlo in una selezione, compilarlo ed eliminare il percorso. Utilizzando lo strumento sposta, spostare il quadrato e centrarlo sul pulsante Chiudi il puntatore del mouse.
6.  Creare un nuovo livello e denominarlo "Play Triangle". Utilizzare lo strumento penna per creare il triangolo per "riprodurre" utilizzando le stesse tecniche effettuate per creare il livello quadrato di chiusura. Centrare il puntatore del mouse sul pulsante di riproduzione.

A questo punto è possibile creare il file di immagine del passaggio del mouse. Nascondi tutti i livelli, quindi Mostra solo i livelli seguenti, in questo ordine (dall'alto verso il basso):

Triangolo di riproduzione

Chiudi quadrato

Esegui il passaggio del mouse

Chiudi il puntatore del mouse

Salvare in un nuovo file usando il comando Salva copia dal menu file. Selezionare l'opzione BMP nella parte Salva come della finestra di dialogo Salva copia e digitare il nome di un file a cui si fa riferimento in un secondo momento nel file di definizione dell'interfaccia personalizzata. Idealmente, è consigliabile salvarlo nella stessa directory del file di definizione dell'interfaccia personalizzata. Ad esempio, è possibile chiamare questo hover.bmp. Scegliere le impostazioni predefinite e salvare il file.

Il file di immagine del passaggio del mouse dovrebbe avere un aspetto simile all'illustrazione seguente.

![immagine del passaggio del mouse](images/absam01h.png)

Il pulsante di spostamento giallo viene visualizzato al posto del pulsante normale. Se si passa il mouse sul pulsante destro dell'interfaccia, viene visualizzato il pulsante giallo con etichetta "Play". Se si passa il puntatore del mouse sul pulsante sinistro, l'utente visualizzerà "close". Le due immagini del passaggio del mouse non verranno mai visualizzate contemporaneamente, perché il mouse non può passare il mouse su entrambi i pulsanti nello stesso momento. È necessario attivare il puntatore del mouse e disporre di un file di immagine del passaggio del mouse che corrisponda alle aree dei file di mapping alle aree del file hover.

Quando si salva il file, il nome file scelto verrà usato in un secondo momento come valore per l'attributo **hoverImage** dell'elemento **ButtonGroup** nel file di definizione dell'interfaccia personalizzata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione della prima interfaccia**](building-your-first-skin.md)
</dt> </dl>

 

 




