---
description: Esempio di DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Esempio di DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72067c04e108354c1706690bc71e8b339ad5af071c46cc0e4102ae10e9a3643f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148724"
---
# <a name="dvapp-sample"></a>Esempio di DVApp

## <a name="description"></a>Descrizione

Applicazione di acquisizione DV (Digital Video).

Questo esempio illustra come compilare vari tipi di grafici di filtro per il controllo dei camcorder DV. Illustra anche come eseguire l'acquisizione, l'anteprima, la trasmissione e il controllo del dispositivo con un camcorder DV.

### <a name="usage"></a>Utilizzo

L'applicazione DVApp supporta le modalità seguenti:

-   Anteprima: esegue il rendering di DV dal camcorder a una finestra video.
-   Da DV a file di tipo 1: acquisisce i dati DV dal camcorder in un file DV di tipo 1.
-   File di tipo 1 in DV: trasmette i dati da un file DV di tipo 1 al camcorder.
-   Da DV a file di tipo 2: acquisisce i dati DV dal camcorder in un file DV di tipo 2.
-   File di tipo 2 in DV: trasmette i dati da un file DV di tipo 2 al camcorder.

Anche le modalità di acquisizione e trasmissione eseguono l'anteprima. Ognuna di queste modalità ha anche **l'opzione Nessuna** anteprima, che disabilita l'anteprima. L'acquisizione senza anteprima è più efficiente e può ridurre il numero di fotogrammi eliminati.

L'applicazione viene avviata in modalità di anteprima. Per selezionare un'altra modalità, scegliere una modalità dal menu **Graph modalità.** Per ogni modalità, DVApp crea un grafo di filtro che supporta la funzionalità di tale modalità. Per salvare il grafo come file GraphEdit (con estensione grf), selezionare Salva Graph **file** dal menu **File.** Uscire da DVApp prima di aprire il file in GraphEdit.

Per acquisire in un file:

1.  Scegliere **Imposta file** di output dal menu **File** e immettere un nome file.
2.  Nel menu **Graph modalità** file selezionare una modalità *da DV* a File (digitare 1 o 2, con o senza anteprima).
3.  Fare clic **su Record**.
4.  Se il camcorder è in modalità VTR, fare clic su **Riproduci**.
5.  Per arrestare l'acquisizione, fare clic **su Arresta**.

Per trasmettere da un file al camcorder:

1.  Scegliere **Imposta file** di input dal menu **File** e selezionare un file DV. Il file deve corrispondere alla modalità selezionata (tipo 1 o tipo 2).
2.  Nel menu **Graph modalità** di avvio selezionare una modalità Da file a *DV* (tipo 1 o 2, con o senza anteprima).
3.  Fare clic su **Esegui**.
4.  Per registrare i dati su nastro, fare clic su **Registra**.
5.  Per interrompere la trasmissione, fare clic su **Arresta**.

Se il camcorder è in modalità VTR, l'utente può controllare il meccanismo di trasporto tramite i pulsanti di tipo VCR dell'applicazione. Per cercare il nastro, immettere il codice temporale di destinazione e fare clic sul pulsante cerca.

Per limitare la quantità di dati che l'applicazione acquisisce, scegliere **Acquisisci dimensioni** dal menu **File.**

Per controllare il formato del nastro (NTSC o PAL), scegliere **Controlla nastro** **dal** menu Opzioni.

Per modificare le dimensioni della finestra di anteprima, scegliere **Modifica** dimensioni decodifica **dal** menu Opzioni.

### <a name="programming-notes"></a>Note sulla programmazione

Lo scopo principale di questa applicazione è mostrare come compilare vari grafici di acquisizione e trasmissione DV.

### <a name="device-arrival-and-removal"></a>Arrivo e rimozione del dispositivo

L'applicazione gestisce l'arrivo e la rimozione del dispositivo usando due tecniche diverse. Per l'arrivo del dispositivo, il ciclo di messaggi dell'applicazione risponde ai messaggi \_ DEVICECHANGE WM. Per la rimozione del dispositivo, l'applicazione risponde agli [**eventi EC \_ DEVICE \_ LOST**](ec-device-lost.md) dal gestore del grafico dei filtri. Entrambi gli approcci funzionano, anche se l'evento EC \_ DEVICE LOST dipende dall'esistenza del dispositivo nel grafico dei \_ filtri.

L'applicazione gestisce un solo dispositivo alla volta. Se il dispositivo corrente viene rimosso, l'applicazione cerca un altro dispositivo DV nel sistema.

In alcuni camcorder DV, l'utente deve arrestare il dispositivo quando lo passa dalla modalità fotocamera alla modalità VTR, che attiva un messaggio di dispositivo perso. L'applicazione risponde abilitando o disabilitando i comandi di menu appropriati. Tuttavia, se l'utente passa rapidamente da una modalità all'altra, il camcorder potrebbe non generare un messaggio di dispositivo perso. È possibile forzare l'aggiornamento dei **menu** scegliendo Modalità di **aggiornamento** dal menu Opzioni. Alcuni camcorder DV possono attivare/disattivare le modalità senza arrestarsi, ma inviare un messaggio di dispositivo perso solo quando passano alla modalità VTR.

### <a name="device-control"></a>Controllo dei dispositivi

La funzionalità del **pulsante Riproduci** **e Registra** dipende dalla modalità corrente:

-   Anteprima: il grafico dei filtri viene eseguito automaticamente. Il **pulsante Riproduci** avvia il trasporto.
-   Acquisisci nel file: il **pulsante Registra** esegue il grafico e il **pulsante Riproduci** avvia il trasporto.
-   Trasmetti al dispositivo: il **pulsante Riproduci** esegue il grafico e il **pulsante Registra** avvia il trasporto.

L'applicazione di esempio non esegue l'acquisizione con precisione dei frame. In vari punti, l'applicazione chiama la **funzione Sospensione** per attendere la risposta del dispositivo. I camcorder DV più recenti inviano una notifica quando lo stato del dispositivo cambia. I dispositivi meno recenti potrebbero non supportare la notifica. ai fini di un esempio, chiamare **Sleep** è una soluzione più semplice.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: *\[ SDK Root \]* Samples \\ Multimedia DirectShow Capture \\ \\ \\ DVApp.This sample is installed under the following path: SDK Root Samples Multimedia DirectShow Capture \\ DVApp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di un camcorder DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



