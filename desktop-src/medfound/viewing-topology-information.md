---
description: Visualizzazione delle informazioni sulla topologia
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Visualizzazione delle informazioni sulla topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fd1d7d28de3d7fa5420241abf793295323532dca29d3d68d1271545aa460dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237373"
---
# <a name="viewing-topology-information"></a>Visualizzazione delle informazioni sulla topologia

In TopoEdit ogni elemento della topologia, ad esempio nodi, input dei nodi e output dei nodi, dispone di un archivio attributi associato che gestisce il comportamento del nodo. Per visualizzare gli attributi, selezionare l'elemento e nel **riquadro Attributi** vengono visualizzate le informazioni. Per le topologie caricate da un file XML, alcuni nodi potrebbero non visualizzare l'intero archivio attributi. Per visualizzare l'intero archivio attributi, risolvere la topologia. Per altre informazioni, vedere [Risoluzione di una topologia con TopoEdit.](resolving-a-topology-with-topoedit.md)

Nella tabella seguente vengono illustrati l'elemento della topologia e gli attributi visualizzati nel riquadro.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento topologia</th>
<th>Attributi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nodi della topologia</td>
<td><ul>
<li><a href="topology-node-attributes.md">Attributi del nodo della topologia</a> per tutti i nodi.<br/></li>
<li><a href="presentation-descriptor-attributes.md">Attributi del descrittore di presentazione</a> solo per i nodi di origine.<br/></li>
<li>Informazioni sull'autorità di attendibilità di input e output per i nodi di trasformazione e output.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Input del nodo</td>
<td><ul>
<li><a href="media-type-attributes.md">Attributi del tipo di supporto</a> per tutti i nodi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Output del nodo</td>
<td><ul>
<li><a href="stream-descriptor-attributes.md">Attributi del descrittore di flusso solo</a> per i nodi di origine.<br/></li>
<li><a href="media-type-attributes.md">Attributi del tipo di supporto</a> per tutti i nodi.<br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

I valori degli attributi, ad eccezione dei riferimenti ai puntatori e dei valori di matrice, possono essere modificati. Per modificare un valore di attributo, digitare il nuovo valore accanto all'attributo e fare clic su **Salva** nel **riquadro Attributi**. Il nuovo valore viene aggiornato nell'archivio attributi e applicato alla topologia solo dopo la risoluzione.

## <a name="to-add-a-new-attribute-for-a-node"></a>Per aggiungere un nuovo attributo per un nodo

1.  Selezionare il nodo facendo clic su di esso nel **riquadro Topologia**.

    Gli attributi impostati nel nodo vengono visualizzati nel riquadro **Attributi**.

2.  Nel riquadro **Attributi fare** clic su **Aggiungi**.

    Verrà visualizzata la **finestra di dialogo Aggiungi** attributo .

3.  Nel primo elenco a discesa scegliere la categoria Attributo.

    Le categorie dipendono dal nodo della topologia. Ad esempio, per il nodo di origine, l'elenco a discesa mostra **Attributi** del descrittore di presentazione e Attributi **nodo** come categorie disponibili.

4.  Nel secondo elenco a discesa scegliere l'attributo che si vuole impostare nel nodo.

5.  Nella casella di modifica aggiungere il valore per l'attributo.

6.  Fare **clic su** Aggiungi per aggiungere l'attributo e tornare alla finestra principale oppure fare clic su **Annulla** per annullare l'operazione.

7.  Scegliere **Risolvi topologia** dal menu Topologia **per** impostare il nuovo attributo sulla topologia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




