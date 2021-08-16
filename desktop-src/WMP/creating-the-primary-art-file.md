---
title: Creazione del file di grafica principale
description: Creazione del file di grafica principale
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- creazione di interfaccia, file di grafica principali
- Windows Media Player, file art
- skins, file art
- file per le interfaccia, grafica
- file di grafica per le interfaccia, immagini primarie
- Windows Media Player, immagini primarie
- interfaccia, immagini primarie
- immagini primarie nelle interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21483e9b39692ad9eee7eb2cd7958f2fa70ddb7c2926877b84f3f537156bd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341540"
---
# <a name="creating-the-primary-art-file"></a>Creazione del file di grafica principale

Il file di grafica principale conterrà l'immagine visualizzata per la prima volta dall'utente dell'interfaccia. In questo caso, si creeranno immagini in diversi livelli del programma di grafica. Il motivo per cui si usano i livelli è che si copieranno livelli specifici in un secondo momento per creare file di mappa e file di grafica alternativi.

Per creare il file di grafica principale, si creeranno i livelli seguenti nell'ordine seguente:

Livello di sfondo dell'interfaccia

Si tratta del colore trasparente quando viene visualizzata l'interfaccia. Creare prima un livello per questo livello, ma scegliere il colore finale di questo livello dopo aver scelto un colore per il livello contenitore dell'interfaccia. Questo colore deve essere simile, ma non uguale al livello del contenitore dell'interfaccia, per nascondere eventuali effetti di anti-aliasing.

Livello contenitore dell'interfaccia

Questa è l'immagine che formerà il contorno dell'interfaccia e sarà ciò che l'utente vede. Sarà anche il contenitore per i due pulsanti in questo esempio. Si pensi all'interfaccia come a un contenitore per i controlli dell'interfaccia utente, ad esempio pulsanti, dispositivi di scorrimento e così via. In questo esempio il contenitore è un ovale giallo.

Livelli dei pulsanti Riproduci e Chiudi

Questi sono i due controlli dell'interfaccia utente utilizzati in questo esempio. I livelli verranno inseriti in livelli separati in modo da poterli modificare facilmente o copiarli in un secondo momento.

Prima di creare i livelli, è necessario creare il file che contenerà i livelli. Avviare Photoshop e creare un nuovo file con un'altezza di 100 pixel e una larghezza di 200 pixel. Il file usato per creare l'immagine per questo esempio è denominato tiny.psd ed è incluso nell'SDK.

Tutte le istruzioni sono fornite in termini di Gif, ma qualsiasi altro programma di grafica può essere usato per creare le interfaccia, purché sia possibile salvare in uno dei formati di file supportati da Windows Media Player (BMP, GIF, JPG e PNG). La creazione dell'interfaccia utente risulta più semplice se si usa un programma di grafica con livelli, ad esempio Adobe Photoshop, Jasc Paint Shop Pro o Jedor Viscosity. I livelli sono estremamente utili perché le immagini devono essere allineate correttamente per il mapping delle immagini e la visualizzazione di immagini alternative.

## <a name="skin-background-layer"></a>Livello di sfondo dell'interfaccia

Creare un nuovo livello e assegnare al livello il nome "Sfondo interfaccia". Questo diventerà il colore di trasparenza che verrà definito nel file di definizione dell'interfaccia. Attendere che venga scelto il colore per il contenitore dell'interfaccia prima di riempire il livello di sfondo dell'interfaccia con un colore specifico.

## <a name="skin-container-layer"></a>Livello contenitore dell'interfaccia

Creare quindi un nuovo livello e chiamarlo "Contenitore interfaccia". Verranno definiti i bordi dell'interfaccia e sarà il contenitore per i pulsanti.

Scegliere un colore di primo piano per la forma usando i dispositivi di scorrimento Colore Web. In questo esempio è stato scelto il \# colore "DBDD11".

Creare quindi una forma ovale. Il modo più semplice è usare lo strumento Eliptical Marquee e creare una selezione ovale. Dopo aver creato una selezione ovale con le dimensioni e la forma desiderate, riempire la selezione con il colore di primo piano e annullare la selezione.

Infine, per rendere questo aspetto un po' più interessante, applicare l'effetto livello Smussato ed Rilievo con i valori predefiniti.

Il livello del contenitore dell'interfaccia dovrebbe essere simile alla figura seguente.

![livello del contenitore di interfaccia](images/g01cont.png)

## <a name="background-skin-color"></a>Colore dell'interfaccia di sfondo

Ora che è stato scelto un colore di primo piano per la forma del contenitore dell'interfaccia, è possibile scegliere un colore simile per il livello di sfondo dell'interfaccia. Non si vuole usare esattamente lo stesso colore oppure anche il contenitore dell'interfaccia sarà trasparente. Assicurarsi infatti di non usare questo colore esatto in nessun altro punto dell'interfaccia, anche nelle fotografie, perché ovunque venga visualizzato questo colore, verrà visualizzata l'immagine desktop.

Si vuole un colore vicino al colore del contenitore dell'interfaccia per evitare effetti di anti-aliasing. Ad esempio, se si ha uno sfondo nero, alcuni bit di nero possono essere visualizzati intorno al bordo dell'interfaccia. Scegliendo un colore vicino al colore del contenitore dell'interfaccia, tutti i pixel smarriti visualizzati nel processo di anti-aliasing non verranno inosservati.

L'anti-aliasing è il processo di smussatura dei bordi di forme smussate o curve. L'anti-aliasing crea nuovi colori, per i pixel lungo i bordi di una forma, che sono una combinazione del colore di primo piano e del colore di sfondo. Alcuni di questi colori possono causare la perdita dei pixel quando il colore di sfondo viene reso trasparente.

Il livello di sfondo dell'interfaccia dovrebbe essere simile alla figura seguente.

![livello dell'interfaccia di sfondo](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Livelli dei pulsanti Riproduci e Chiudi

Creare un nuovo livello e assegnare al livello il nome "Chiudi pulsante". Usando di nuovo lo strumento di selezione Eliptical Marquee (Cornice ellittica), creare un cerchio e posizionarlo sul lato sinistro dell'immagine complessiva. Attivare la visibilità del file contenitore dell'interfaccia per consentire di posizionare la selezione.

Quando si è soddisfatti del posizionamento, riempire la selezione con qualsiasi colore (ad eccezione del colore del contenitore dell'interfaccia o dello sfondo dell'interfaccia). In questo esempio è stato scelto un colore viola. Non è necessario ricordare il numero del colore. Annullare quindi la selezione e applicare un altro effetto predefinito del livello Smussatura ed Rilievo. Se si vogliono applicare effetti non di livello al pulsante, creare una copia dell'originale per un uso successivo nel mapping.

Il pulsante Chiudi dovrebbe essere simile alla figura seguente.

![pulsante di chiusura](images/g01qbut.png)

Creare un nuovo livello e assegnare al livello il nome "Pulsante Riproduci". Usare le stesse tecniche usate per il pulsante Chiudi, ma assegnargli un colore diverso. In questo caso, è stato scelto un colore di pulsante rosa, ma è possibile usare qualsiasi colore purché non sia lo stesso colore del contenitore dell'interfaccia (perché si fondono nel contenitore) o il colore di sfondo dell'interfaccia (perché diventerebbe trasparente).

Il pulsante Riproduci dovrebbe essere simile alla figura seguente.

![pulsante di riproduzione](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Combinare i livelli e salvare

A questo punto si è pronti per creare il file di grafica principale. Nascondere tutti i livelli e quindi visualizzare solo i livelli seguenti, in questo ordine (dall'alto verso il basso):

Pulsante Riproduci

Pulsante Chiudi

Contenitore di interfaccia

Sfondo dell'interfaccia

Salvare in un nuovo file usando il comando Salva copia dal menu File. Selezionare l'opzione BMP nella parte Salva con nome della finestra di dialogo Salva una copia e digitare un nome di file a cui si farà riferimento in seguito nel file di definizione dell'interfaccia. Idealmente, è consigliabile salvarlo nella stessa directory del file di definizione dell'interfaccia. Ad esempio, è possibile chiamare questo background.bmp. Scegliere le impostazioni predefinite e salvare il file.

Il file di grafica principale dovrebbe essere simile al seguente:

![file di grafica principale](images/g01prime.png)

Questo nome file verrà utilizzato come valore per l'attributo **backgroundImage** **dell'elemento VIEW** nel file di definizione dell'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione della prima interfaccia**](building-your-first-skin.md)
</dt> </dl>

 

 




