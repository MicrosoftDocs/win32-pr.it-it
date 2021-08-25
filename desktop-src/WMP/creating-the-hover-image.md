---
title: Creazione dell'immagine al passaggio del mouse
description: Creazione dell'immagine al passaggio del mouse
ms.assetid: 169a99ba-96a0-4487-aa1c-07c83c0bc237
keywords:
- creazione di skin, immagini al passaggio del mouse
- Windows Media Player skin, file art
- skins, file di grafica
- file per skin, art
- file di grafica per le skin, immagini al passaggio del mouse
- Windows Media Player, immagini al passaggio del mouse
- skin, immagini al passaggio del mouse
- immagini al passaggio del mouse nelle skin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88eff91123a28dae94425d7ea6e7591462545a2d7da0372b088eeec6bd67ed60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902281"
---
# <a name="creating-the-hover-image"></a>Creazione dell'immagine al passaggio del mouse

L'immagine principale di questa interfaccia è due pulsanti che siede su un ovale. Per fornire all'utente un'idea di cosa fare, è possibile aggiungere immagini al passaggio del mouse. Si tratta di immagini alternative che vengono visualizzate quando l'utente passa il mouse su un pulsante. I pulsanti al passaggio del mouse conterranno anche i simboli di controllo di riproduzione e arresto del videoregistratore in modo che gli utenti sappiano esattamente cosa possono fare. L'uso di immagini al passaggio del mouse consente di creare skin complesse, auto documentali e di arte.

Per creare l'immagine al passaggio del mouse, è necessario prendere i due pulsanti creati per il file di grafica principale, copiarli nei nuovi livelli e aggiungere altri livelli per il testo. Eseguire la procedura descritta di seguito:

1.  Copiare il livello del pulsante Chiudi e rinominarlo "Chiudi al passaggio del mouse".
2.  Usare il Selezione colori per creare un colore di primo piano di un giallo chiaro ( \# CCFF33). Questa opzione è stata scelta per il contrasto con i colori dei pulsanti. Usare quindi lo strumento Paint bucket per riempire l'interno del cerchio nel livello Chiudi al passaggio del mouse.
3.  Copiare il livello del pulsante Riproduci e rinominarlo "Riproduci al passaggio del mouse".
4.  Usare lo Paint bucket per riempire l'interno del cerchio nel livello Play hover con lo stesso colore del cerchio al passaggio del mouse Close.
5.  Creare un nuovo livello e assegnarle il nome "Chiudi quadrato". Usare il Selezione colori per creare un colore primo piano di blu scuro. Usare lo strumento penna per disegnare un quadrato, trasformarlo in una selezione, riempirlo ed eliminare il tracciato. Usando lo strumento Sposta, spostare il quadrato e centrarlo sul pulsante Chiudi al passaggio del mouse.
6.  Creare un nuovo livello e assegnarle il nome "Riproduci triangolo". Usare lo strumento penna per creare il triangolo per "Play" usando le stesse tecniche usate per creare il livello quadrato Chiudi. Centrarla sul pulsante Riproduci al passaggio del mouse.

A questo punto è possibile creare il file hover art. Nascondere tutti i livelli e quindi visualizzare solo i livelli seguenti in questo ordine (dall'alto verso il basso):

Triangolo di riproduzione

Chiudi quadrato

Riproduci al passaggio del mouse

Chiudere il passaggio del mouse

Salvare in un nuovo file usando il comando Salva copia dal menu File. Selezionare l'opzione BMP nella parte Salva con nome della finestra di dialogo Salva una copia e digitare un nome di file a cui si farà riferimento in un secondo momento nel file di definizione dell'interfaccia. Idealmente è consigliabile salvarlo nella stessa directory del file di definizione dell'interfaccia. Ad esempio, è possibile chiamare questo hover.bmp. Scegliere le impostazioni predefinite e salvare il file.

Il file di disegno al passaggio del mouse dovrebbe essere simile a quello illustrato nella figura seguente.

![immagine al passaggio del mouse](images/absam01h.png)

Il pulsante giallo al passaggio del mouse verrà visualizzato al posto del pulsante normale. Se si passa il puntatore del mouse sul pulsante destro nell'interfaccia, viene visualizzato il pulsante giallo con etichetta "Play" e, se si passa il mouse sul pulsante sinistro, l'utente visualizza "Chiudi". Le due immagini al passaggio del mouse non verranno mai visualizzate contemporaneamente, perché il mouse non può passare il mouse su entrambi i pulsanti contemporaneamente. È necessario attivare il passaggio del mouse e disporre di un file di disegno al passaggio del mouse che corrisponda alle aree dei file di mapping alle aree del file al passaggio del mouse.

Quando si salva il file, il nome file scelto verrà usato in un secondo momento come valore per l'attributo **hoverImage** **dell'elemento BUTTONGROUP** nel file di definizione dell'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione della prima interfaccia**](building-your-first-skin.md)
</dt> </dl>

 

 




