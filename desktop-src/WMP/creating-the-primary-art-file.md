---
title: Creazione del file di immagine principale
description: Creazione del file di immagine principale
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- creazione di interfacce, file di immagine principali
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, immagini primarie
- Windows Media Player Skin, immagini primarie
- interfacce, immagini primarie
- immagini primarie nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104557334"
---
# <a name="creating-the-primary-art-file"></a>Creazione del file di immagine principale

Il file di immagine principale conterrà l'immagine che l'utente dell'interfaccia vede per primo. In questo caso, verranno create immagini in diversi livelli del programma Art. Il motivo per l'uso dei livelli è che i livelli specifici vengono copiati in un secondo momento per creare file di mapping e file di grafica alternativi.

Per creare il file di immagine principale, si creeranno i livelli seguenti nell'ordine seguente:

Livello sfondo interfaccia

Si tratta del colore che sarà trasparente quando verrà visualizzata l'interfaccia. Per prima cosa, creare un livello, ma scegliere il colore finale del livello dopo aver scelto un colore per il livello contenitore dell'interfaccia. Questo colore deve essere simile a, ma non allo stesso modo del livello contenitore dell'interfaccia, per nascondere eventuali effetti anti-aliasing.

Livello contenitore interfaccia

Si tratta dell'immagine che formerà il contorno dell'interfaccia e sarà ciò che viene visualizzato dall'utente. In questo esempio sarà anche il contenitore per i due pulsanti. Si pensi alla propria interfaccia come a un contenitore per i controlli dell'interfaccia utente, ad esempio pulsanti, dispositivi di scorrimento e così via. In questo esempio, il contenitore è un ovale giallo.

Livelli pulsante Riproduci e Chiudi

Questi sono i due controlli dell'interfaccia utente usati in questo esempio. Si inseriranno in livelli distinti per poterli modificare facilmente o copiarli in un secondo momento.

Prima di creare i livelli, è necessario creare il file che conterrà i livelli. Avviare Photoshop e creare un nuovo file con dimensioni massime di 100 pixel e 200 pixel di larghezza. Il file utilizzato per creare l'immagine per questo esempio è denominato tiny.psd ed è incluso nell'SDK.

Tutte le istruzioni sono fornite in termini di Photoshop, ma è possibile usare qualsiasi altro programma artistico per creare interfacce, purché sia possibile salvare in uno dei formati di file supportati da Windows Media Player (BMP, GIF, JPG e PNG). La creazione di Skin è più semplice se si usa un programma artistico con livelli, ad esempio Adobe Photoshop, Jasc Paint Shop Pro o la viscosità di Jedor. I livelli sono estremamente utili perché le immagini devono essere allineate correttamente per il mapping delle immagini e la visualizzazione di immagini alternative.

## <a name="skin-background-layer"></a>Livello sfondo interfaccia

Creare un nuovo livello e denominarlo "sfondo interfaccia". Questo diventerà il colore di trasparenza che verrà definito nel file di definizione dell'interfaccia. Attendere che il colore per il contenitore di Skin venga scelto prima di riempire il livello di sfondo dell'interfaccia con un colore specifico.

## <a name="skin-container-layer"></a>Livello contenitore interfaccia

Successivamente, creare un nuovo livello e chiamarlo "contenitore di skin". Verranno definiti i bordi dell'interfaccia e sarà il contenitore per i pulsanti.

Scegliere un colore di primo piano per la forma utilizzando i dispositivi di scorrimento dei colori Web. In questo esempio \# è stato scelto il colore "DBDD11".

Successivamente, creare una forma ovale. Il modo più semplice consiste nell'usare lo strumento ellittica Marquee e creare una selezione ovale. Quando è stata creata una selezione ovale che rappresenta le dimensioni e la forma desiderate, riempire la selezione con il colore di primo piano e annullare la selezione.

Infine, per rendere questo aspetto leggermente più interessante, applicare l'effetto del livello di smussatura e rilievo con i valori predefiniti.

Il livello del contenitore dell'interfaccia utente dovrebbe essere simile a quello illustrato nella figura seguente.

![livello contenitore interfaccia](images/g01cont.png)

## <a name="background-skin-color"></a>Colore della pelle di sfondo

Ora che è stato scelto un colore di primo piano per la forma del contenitore di skin, è possibile scegliere un colore simile per il livello di sfondo della pelle. Non si vuole esattamente lo stesso colore o il contenitore Skin sarà anche trasparente. In realtà, assicurarsi di non usare questo colore esatto in qualsiasi altra parte dell'interfaccia, neanche nelle fotografie, perché ogni volta che viene visualizzato questo colore, viene visualizzata l'immagine del desktop.

Si desidera un colore vicino al colore del contenitore dell'interfaccia per evitare effetti anti-aliasing. Se, ad esempio, si dispone di uno sfondo nero, alcuni bit del nero possono apparire intorno al bordo della pelle. Scegliendo un colore vicino al colore del contenitore dell'interfaccia, eventuali pixel randagi visualizzati nel processo di anti-aliasing non verranno rilevati.

L'anti-aliasing è il processo di smussatura dei bordi delle forme inclinate o curve. L'anti-aliasing crea nuovi colori, per pixel lungo i bordi di una forma, ovvero una combinazione del colore di primo piano e del colore di sfondo. Alcuni di questi colori possono causare la mancata presenza di pixel quando il colore di sfondo viene reso trasparente.

Il livello dello sfondo dell'interfaccia utente dovrebbe essere simile a quello illustrato nella figura seguente.

![livello interfaccia di sfondo](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Livelli pulsante Riproduci e Chiudi

Creare un nuovo livello e denominarlo "Chiudi pulsante". Utilizzando di nuovo lo strumento ellittica Marquee Selection, creare un cerchio e posizionarlo sul lato sinistro dell'immagine complessiva. Attivare la visibilità del file contenitore dell'interfaccia per facilitare la selezione.

Quando si è soddisfatti della posizione, riempire la selezione con qualsiasi colore, ad eccezione del colore del contenitore o dello sfondo dell'interfaccia. In questo esempio è stato scelto un colore viola. Non è necessario ricordare il numero di colore. Annullare quindi la selezione e applicare un altro effetto del livello di rilievo e smussatura predefinito. Se si desidera applicare effetti non di livello al pulsante, creare una copia dell'originale per utilizzarlo in un secondo momento nel mapping.

Il pulsante Chiudi avrà un aspetto simile a quello illustrato nella figura seguente.

![pulsante di chiusura](images/g01qbut.png)

Creare un nuovo livello e denominarlo "pulsante Riproduci". Utilizzare le stesse tecniche effettuate per il pulsante Chiudi, ma assegnare un colore diverso. In questo caso, è stato scelto il colore di un pulsante rosa, ma è possibile usare qualsiasi colore, purché non sia lo stesso colore del contenitore di Skin (perché si mescolerà nel contenitore) o il colore di sfondo dell'interfaccia (perché diventerebbe trasparente).

Il pulsante Riproduci avrà un aspetto simile a quello illustrato nella figura seguente.

![pulsante Riproduci](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Combinare i livelli e salvare

A questo punto è possibile creare il file di immagine principale. Nascondi tutti i livelli e Mostra solo i livelli seguenti, in questo ordine (dall'alto verso il basso):

Pulsante Riproduci

Pulsante Chiudi

Contenitore Skin

Sfondo interfaccia

Salvare in un nuovo file usando il comando Salva copia dal menu file. Selezionare l'opzione BMP nella parte Salva come della finestra di dialogo Salva copia e digitare il nome di un file a cui si fa riferimento in un secondo momento nel file di definizione dell'interfaccia personalizzata. Idealmente, è consigliabile salvarlo nella stessa directory del file di definizione dell'interfaccia personalizzata. Ad esempio, è possibile chiamare questo background.bmp. Scegliere le impostazioni predefinite e salvare il file.

Il file di immagine principale dovrebbe essere simile al seguente:

![file di immagine principale](images/g01prime.png)

Questo nome file verrà usato come valore per l'attributo **BackgroundImage** dell'elemento **View** nel file di definizione dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione della prima interfaccia**](building-your-first-skin.md)
</dt> </dl>

 

 




