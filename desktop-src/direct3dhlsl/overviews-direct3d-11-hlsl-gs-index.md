---
title: Come indicizzare più output Flussi
description: Nel modello shader 5, uno shader geometry può supportare fino a 4 flussi separati. Ciò significa che un singolo shader può eseguire l'output tra uno e quattro flussi di output, a seconda del numero di flussi dichiarati.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37aefd8b7cdcab05515bda6f81fa6c679751dc95
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473397"
---
# <a name="how-to-index-multiple-output-streams"></a>Procedura: Indicizzare più output Flussi

Nel modello shader 5, uno shader geometry può supportare fino a 4 flussi separati. Ciò significa che un singolo shader può eseguire l'output tra uno e quattro flussi di output, a seconda del numero di flussi dichiarati.

Per indicizzare più flussi di output

1.  Definire un flusso di dati usando un tipo di modello di flusso.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Definire un secondo flusso di dati usando un tipo di modello di flusso.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Eseguire l'output dei dati in uno o entrambi i flussi usando le funzioni intrinseche dell'oggetto di output del flusso, ad esempio Append o RestartStrip.

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

Quando si usa un singolo flusso di output, è possibile creare strisce triangolare, strisce di linee o elenchi di punti. Quando si archiviano le strisce triangolo e linea nel buffer di uscita del flusso, queste vengono espanse rispettivamente in elenchi di triangoli e linee. È anche possibile rasterizzare un flusso e non inviarlo a un buffer di memoria.

Quando si usano più flussi di output, tutti i flussi devono contenere punti e al rasterizzatore è possibile inviare fino a un flusso di output. Più comunemente, un'applicazione non rasterizza alcun flusso.

Dopo aver trasmesso i dati in un buffer, è possibile usare questi dati per eseguire il rendering di qualsiasi tipo primitivo, non solo del tipo primitivo usato per riempire il buffer.

L'output totale dello shader geometry è limitato a 1024 scalari. Se sono presenti più flussi, il numero di scalari viene calcolato dal tipo di flusso più grande moltiplicato per il numero massimo di vertici.




| | | Differenze tra il modello shader 4 e il modello shader 5:<br /> Modello shader 4:<br /><ul><li>Il numero massimo di scalari per l'output del flusso è 64.</li><li>La maschera del registro per componente deve corrispondere nell'intervallo di indici.</li></ul>Modello shader 5:<br /><ul><li>Il numero massimo di scalari per l'output del flusso è 128.</li><li>Non è necessario che la maschera del registro per componente corrisponda nell'intervallo di indici.</li><li>L'indicizzazione dinamica degli output deve essere legale in tutti i flussi.</li><li>Non è necessario che le modalità di interpolazione corrispondano per i flussi.</li></ul> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità geometry shader](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





