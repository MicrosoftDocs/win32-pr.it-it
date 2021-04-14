---
description: Aggiunta di nodi Transform con TopoEdit
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: Aggiunta di nodi Transform con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fa39457f8808070f93a4e5de31e181525ca33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343766"
---
# <a name="adding-transform-nodes-with-topoedit"></a>Aggiunta di nodi Transform con TopoEdit

Un nodo Transform rappresenta una trasformazione Media Foundation (MFT) che elabora i dati multimediali ricevuti da un nodo di origine. Quando è pronto, la pipeline la passa al nodo di output per il rendering. In Media Foundation, codificatori, decodificatori, multiplexer, demultiplexer e effetti video audio vengono implementati come MFTs. TopoEdit supporta l'aggiunta di nodi di trasformazione che rappresentano MFTs registrati e personalizzati.

Per informazioni sull'aggiunta di nodi Transform a livello di codice usando le API di Media Foundation, vedere [creazione di nodi di trasformazione](creating-transform-nodes.md).

## <a name="to-add-a-registered-mft-to-the-topology"></a>Per aggiungere una MFT registrata alla topologia

1.  Scegliere **Aggiungi trasformazione** dal menu **topologia** .

    Verrà visualizzata la finestra di dialogo **Seleziona trasformazione** . Viene visualizzato un elenco categorizzato dei MFTs registrati che vengono generati enumerando le voci registrate nel registro di sistema chiamando la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .

2.  Espandere la categoria e selezionare il MFT che si desidera aggiungere alla topologia.

3.  Fare clic su **OK** per chiudere la finestra di dialogo e tornare al **riquadro topologia**.

TopoEdit crea il nodo Transform specificato. Il **riquadro topologia** Mostra il nodo trasforma come una casella verde che Visualizza il nome della MFT.

## <a name="to-add-a-custom-mft-to-the-topology"></a>Per aggiungere un MFT personalizzato alla topologia

1.  Nel menu **topologia** fare clic su **Aggiungi MFT personalizzato**.

    Verrà visualizzata la finestra di dialogo **GUID personalizzato di input** .

2.  Nel campo **GUID:** immettere il GUID del MFT che si desidera aggiungere alla topologia.

    > [!Note]  
    > TopoEdit prevede il GUID nel formato "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". In caso contrario, non sarà possibile aggiungere il nodo e verrà visualizzato un messaggio di errore "GUID non valido".

     

3.  Fare clic su **OK** per chiudere la finestra di dialogo e tornare al **riquadro topologia**.

TopoEdit crea il nodo Transform specificato. Il **riquadro topologia** Mostra il nodo trasforma come una casella verde che Visualizza il nome della MFT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di topologie tramite TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



