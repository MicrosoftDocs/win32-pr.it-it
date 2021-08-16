---
description: Creazione di una topologia di riproduzione con TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Creazione di una topologia di riproduzione con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a71ae353c11108fe7c844d8ddd6441e652e007646b91f44c6fe2b480a22a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035429"
---
# <a name="building-a-playback-topology-with-topoedit"></a>Creazione di una topologia di riproduzione con TopoEdit

TopoEdit può creare una topologia di riproduzione per un file multimediale locale aggiungendo e connettendo automaticamente i nodi di origine, trasformazione e output. TopoEdit non risolve automaticamente la topologia. Per riprodurre la topologia, risolverla e quindi usare i controlli di trasporto.

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>Per compilare e riprodurre una topologia per un file multimediale

1.  Scegliere **Esegui** rendering file dal menu **File**.

    Verrà visualizzata la **finestra di dialogo Seleziona origine** supporto .

2.  Passare alla cartella in cui si trova il file multimediale.
3.  Nel **campo Nome file:** immettere il nome del file.
4.  Fare clic su **Apri**.

    Il **riquadro Topologia mostra** la topologia connessa. Internamente, TopoEdit esegue le attività seguenti:

    -   Enumera i flussi nel file multimediale e crea i nodi di origine.
    -   A seconda del tipo di supporto dei nodi di origine, aggiunge nodi di trasformazione, ad esempio decodificatori.
    -   Aggiunge il sink SAR (Streaming Audio Renderer) per il flusso audio e il sink EVR (Enhanced Video Renderer) per il flusso video.
    -   Connette gli input del nodo e gli output del nodo.

5.  Scegliere **Risolvi topologia** dal menu **Topologia**.
6.  Fare clic **sul pulsante** Riproduci sulla barra degli strumenti per riprodurre la topologia. L'immagine seguente mostra il **pulsante** Riproduci :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli di riproduzione in TopoEdit](playback-controls-in-topoedit.md)
</dt> <dt>

[Risoluzione di una topologia con TopoEdit](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



