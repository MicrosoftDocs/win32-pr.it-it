---
description: Esempio DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Esempio DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124827"
---
# <a name="dvapp-sample"></a>Esempio DVApp

## <a name="description"></a>Descrizione

Applicazione di acquisizione video digitale (DV).

Questo esempio illustra come creare vari tipi di grafici di filtro per il controllo di videocamere DV. Viene inoltre illustrato come eseguire il controllo di acquisizione, anteprima, trasmissione e dispositivo con una videocamera DV.

### <a name="usage"></a>Utilizzo

L'applicazione DVApp supporta le modalità seguenti:

-   Anteprima: esegue il rendering di DV dalla videocamera a una finestra del video.
-   Da DV a file di tipo-1: acquisisce i dati DV dalla videocamera in un file DV di tipo 1.
-   Digitare-1 file in DV: trasmette i dati da un file DV di tipo 1 alla videocamera.
-   Da DV a file di tipo 2: acquisisce i dati DV dalla videocamera a un file DV di tipo 2.
-   Digitare-2 file in DV: trasmette i dati da un file DV di tipo 2 alla videocamera.

Anche le modalità di acquisizione e trasmissione eseguono l'anteprima. Ognuna di queste modalità non include anche un'opzione di **Anteprima** , che disabilita l'anteprima. L'acquisizione senza anteprima è più efficiente e può ridurre il numero di frame eliminati.

L'applicazione viene avviata in modalità di anteprima. Per selezionare un'altra modalità, scegliere una modalità dal menu **modalità grafico** . Per ogni modalità, DVApp compila un grafico di filtro che supporta la funzionalità di tale modalità. Per salvare il grafico come file GraphEdit (. GRF), selezionare **Salva grafico in file** dal menu **file** . Uscire da DVApp prima di aprire il file in GraphEdit.

Per acquisire in un file:

1.  Scegliere **Imposta file di output** dal menu **file** e immettere un nome file.
2.  Dal menu **modalità grafico** selezionare un *DV in modalità file* (digitare 1 o digitare 2, con o senza anteprima).
3.  Fare clic su **record**.
4.  Se la videocamera è in modalità VTR, fare clic su **Riproduci**.
5.  Per arrestare l'acquisizione, fare clic su **Arresta**.

Per trasmettere da un file alla videocamera:

1.  Scegliere **Imposta file di input** dal menu **file** e selezionare un file DV. Il file deve corrispondere alla modalità selezionata (tipo 1 o tipo 2).
2.  Dal menu **modalità grafico** selezionare un *file in modalità DV* (digitare 1 o digitare 2, con o senza anteprima).
3.  Fare clic su **Esegui**.
4.  Per registrare i dati su nastro, fare clic su **registra**.
5.  Per arrestare la trasmissione, fare clic su **Arresta**.

Se la videocamera è in modalità VTR, l'utente può controllare il meccanismo di trasporto tramite i pulsanti di tipo VCR dell'applicazione. Per cercare il nastro, immettere il timecode di destinazione e fare clic sul pulsante Seek (Cerca).

Per limitare la quantità di dati che l'applicazione acquisisce, scegliere **dimensioni acquisizione** dal menu **file** .

Per controllare il formato del nastro (NTSC o PAL), scegliere **Controlla nastro** dal menu **Opzioni** .

Per modificare le dimensioni della finestra di anteprima, scegliere **modifica dimensioni decodifica** dal menu **Opzioni** .

### <a name="programming-notes"></a>Note sulla programmazione

Lo scopo principale di questa applicazione è mostrare come compilare diversi grafici di acquisizione e trasmissione DV.

### <a name="device-arrival-and-removal"></a>Arrivo e rimozione del dispositivo

L'applicazione gestisce l'arrivo e la rimozione dei dispositivi, usando due tecniche diverse. Per l'arrivo del dispositivo, il ciclo di messaggi dell'applicazione risponde ai \_ messaggi WM DEVICECHANGE. Per la rimozione dei dispositivi, l'applicazione risponde agli eventi di [**\_ \_ perdita del dispositivo EC**](ec-device-lost.md) dal gestore del grafico dei filtri. Entrambi gli approcci funzionano, sebbene l' \_ \_ evento di perdita del dispositivo EC dipenda dall'esistenza del dispositivo nel grafico dei filtri.

L'applicazione gestisce solo un dispositivo alla volta. Se il dispositivo corrente viene rimosso, l'applicazione cerca un altro dispositivo DV nel sistema.

In alcuni camcorder DV, l'utente deve spegnere il dispositivo quando lo passa tra la modalità videocamera e la modalità VTR, che attiva un messaggio perso dal dispositivo. L'applicazione risponde abilitando o disabilitando i comandi di menu appropriati. Tuttavia, se l'utente passa rapidamente tra le modalità, la videocamera potrebbe non generare un messaggio perso dal dispositivo. È possibile forzare l'aggiornamento dei menu scegliendo **modalità di aggiornamento** dal menu **Opzioni** . Alcuni camcorder DV possono attivare o disattivare le modalità senza arrestare, ma inviare un messaggio perso dal dispositivo solo quando passano alla modalità VTR.

### <a name="device-control"></a>Controllo dei dispositivi

La funzionalità del pulsante **Riproduci** e **registra** dipende dalla modalità corrente:

-   Anteprima: il grafico del filtro viene eseguito automaticamente. Il pulsante **Riproduci** avvia il trasporto.
-   Acquisisci nel file: il pulsante **registra** esegue il grafico e il pulsante **Riproduci** avvia il trasporto.
-   Trasmissione al dispositivo: il pulsante **Riproduci** esegue il grafico e il pulsante **registra** avvia il trasporto.

L'applicazione di esempio non esegue un'acquisizione accurata del frame. In vari punti, l'applicazione chiama la funzione di **sospensione** per attendere la risposta del dispositivo. I camcorder DV più recenti inviano una notifica quando lo stato del dispositivo cambia. I dispositivi meno recenti potrebbero non supportare la notifica; ai fini di un esempio, la chiamata a **Sleep** è una soluzione più semplice.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: *\[ SDK \] radice* \\ esempi \\ Multimedia \\ DirectShow \\ Capture \\ DVApp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



