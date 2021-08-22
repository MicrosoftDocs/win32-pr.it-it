---
description: Aggiunta di nodi di trasformazione con TopoEdit
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: Aggiunta di nodi di trasformazione con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9357b08230b706dc9215cebdbc60d226cadaf0a3f1d7b29f533324ae2e3b1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664931"
---
# <a name="adding-transform-nodes-with-topoedit"></a>Aggiunta di nodi di trasformazione con TopoEdit

Un nodo di trasformazione rappresenta Media Foundation transform (MFT) che elabora i dati multimediali ricevuti da un nodo di origine. Quando è pronta, la pipeline la passa al nodo di output per il rendering. In Media Foundation codificatori, decodificatori, multiplexer, de-multiplexer ed effetti video audio vengono implementati come MFT. TopoEdit supporta l'aggiunta di nodi di trasformazione che rappresentano MFT sia registrati che personalizzati.

Per informazioni sull'aggiunta di nodi di trasformazione a livello di codice Media Foundation API, vedere [Creazione di nodi di trasformazione.](creating-transform-nodes.md)

## <a name="to-add-a-registered-mft-to-the-topology"></a>Per aggiungere un MFT registrato alla topologia

1.  Scegliere **Aggiungi trasformazione** dal menu **Topologia**.

    Verrà **visualizzata la finestra** di dialogo Seleziona trasformazione. Visualizza un elenco categorizzato di MFT registrati che viene generato enumerando le voci registrate nel Registro di sistema chiamando la [**funzione MFTEnum.**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)

2.  Espandere la categoria e selezionare il MFT che si vuole aggiungere alla topologia.

3.  Fare **clic su OK** per chiudere la finestra di dialogo e tornare al riquadro **Topologia**.

TopoEdit crea il nodo di trasformazione specificato. Il **riquadro Topologia mostra** il nodo di trasformazione sotto forma di casella verde che visualizza il nome del MFT.

## <a name="to-add-a-custom-mft-to-the-topology"></a>Per aggiungere un MFT personalizzato alla topologia

1.  Scegliere **Aggiungi MFT** personalizzato dal menu **Topologia**.

    Verrà visualizzata la **finestra di dialogo INPUT GUID** personalizzato .

2.  Nel **campo GUID:** immettere il GUID del MFT che si vuole aggiungere alla topologia.

    > [!Note]  
    > TopoEdit prevede che il GUID sia nel formato "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". In caso contrario, non riesce ad aggiungere il nodo e viene visualizzato un messaggio di errore "GUID non valido".

     

3.  Fare **clic su OK** per chiudere la finestra di dialogo e tornare al riquadro **Topologia**.

TopoEdit crea il nodo di trasformazione specificato. Il **riquadro Topologia mostra** il nodo di trasformazione sotto forma di casella verde che visualizza il nome del MFT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di topologie tramite TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



