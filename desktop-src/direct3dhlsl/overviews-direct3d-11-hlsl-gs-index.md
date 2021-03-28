---
title: Come indicizzare più flussi di output
description: In Shader Model 5 un geometry shader può supportare fino a 4 flussi distinti. Ciò significa che un singolo shader può restituire un output compreso tra uno e quattro flussi di output, a seconda del numero di flussi dichiarati.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044187"
---
# <a name="how-to-index-multiple-output-streams"></a>Procedura: indicizzare più flussi di output

In Shader Model 5 un geometry shader può supportare fino a 4 flussi distinti. Ciò significa che un singolo shader può restituire un output compreso tra uno e quattro flussi di output, a seconda del numero di flussi dichiarati.

Per indicizzare più flussi di output

1.  Definire un flusso di dati utilizzando un tipo di modello di flusso.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Definire un secondo flusso di dati utilizzando un tipo di modello di flusso.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Inviare i dati a (o entrambi) a flussi usando le funzioni intrinseche degli oggetti di output del flusso (ad esempio, Append o RestartStrip).

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

    

Quando si usa un singolo flusso di output, è possibile emettere strisce triangolari, strisce o elenchi di punti. Quando si archiviano le strisce a triangolo e a linee nel buffer di flusso out, queste vengono espanse rispettivamente negli elenchi a triangolo e a linee. È anche possibile rasterizzare un flusso e non inviarlo a un buffer di memoria.

Quando si usano più flussi di output, tutti i flussi devono contenere punti e fino a un flusso di output può essere inviato al rasterizzatore. Più comunemente, un'applicazione non Rasterizza alcun flusso.

Dopo avere trasmesso i dati a un buffer, è possibile usare tali dati per eseguire il rendering di qualsiasi tipo primitivo, non solo del tipo primitivo usato per riempire il buffer.

L'output totale dello shader Geometry è limitato a 1024 valori scalari. Quando sono presenti più flussi, il numero di scalari viene calcolato dal tipo di flusso più grande moltiplicato per il numero massimo di vertici.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra il modello di Shader 4 e il modello di shader 5:<br/> Modello Shader 4:<br/>
<ul>
<li>Il numero massimo di scalari per l'output del flusso è 64.</li>
<li>La maschera di registro per componente deve corrispondere nell'intervallo di indici.</li>
</ul>
Modello Shader 5:<br/>
<ul>
<li>Il numero massimo di scalari per l'output del flusso è 128.</li>
<li>Non è necessario che la maschera di registro per componente corrisponda nell'intervallo di indici.</li>
<li>L'indicizzazione dinamica degli output deve essere valida in tutti i flussi.</li>
<li>Non è necessario che le modalità di interpolazione corrispondano per i flussi.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Geometry shader](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





