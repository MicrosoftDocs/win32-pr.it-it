---
description: Compilazione di una topologia di riproduzione con TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Compilazione di una topologia di riproduzione con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320211"
---
# <a name="building-a-playback-topology-with-topoedit"></a>Compilazione di una topologia di riproduzione con TopoEdit

TopoEdit può compilare una topologia di riproduzione per un file multimediale locale aggiungendo e connettendo automaticamente i nodi di origine, trasformazione e output. TopoEdit non risolve automaticamente la topologia. Per riprodurre la topologia, risolverla e quindi usare i controlli di trasporto.

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>Per compilare e riprodurre una topologia per un file multimediale

1.  Scegliere **file di rendering** dal menu **file** .

    Verrà visualizzata la finestra di dialogo **Seleziona origine multimediale** .

2.  Passare alla cartella in cui si trova il file multimediale.
3.  Nel campo **nome file:** immettere il nome del file.
4.  Fare clic su **Apri**.

    Il **riquadro topologia** Mostra la topologia connessa. Internamente, TopoEdit esegue le attività seguenti:

    -   Enumera i flussi nel file multimediale e crea i nodi di origine.
    -   A seconda del tipo di supporto dei nodi di origine, aggiunge i nodi di trasformazione, ad esempio i decodificatori.
    -   Consente di aggiungere il sink di streaming audio renderer (SAR) per il flusso audio e il sink EVR (Enhanced video renderer) per il flusso video.
    -   Connette gli input del nodo e gli output del nodo.

5.  Scegliere **Risolvi topologia** dal menu **topologia** .
6.  Fare clic sul pulsante **Riproduci** sulla barra degli strumenti per riprodurre la topologia. La figura seguente mostra il pulsante **Riproduci** :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli di riproduzione in TopoEdit](playback-controls-in-topoedit.md)
</dt> <dt>

[Risoluzione di una topologia con TopoEdit](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



