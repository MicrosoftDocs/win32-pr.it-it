---
description: Visualizzazione delle informazioni sulla topologia
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Visualizzazione delle informazioni sulla topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c4e6808fb2414de14817c63f9f4736acc9223f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310161"
---
# <a name="viewing-topology-information"></a>Visualizzazione delle informazioni sulla topologia

In TopoEdit, a ogni elemento della topologia, ad esempio nodi, input del nodo e output del nodo, è associato un archivio attributi che gestisce il comportamento del nodo. Per visualizzare gli attributi, selezionare l'elemento e nel **riquadro attributi** vengono visualizzate le informazioni. Per le topologie caricate da un file XML, è possibile che alcuni nodi non visualizzino l'intero archivio di attributi. Per visualizzare l'intero archivio attributi, risolvere la topologia. Per ulteriori informazioni, vedere la pagina relativa alla [risoluzione di una topologia con TopoEdit](resolving-a-topology-with-topoedit.md).

Nella tabella seguente vengono illustrati l'elemento della topologia e gli attributi visualizzati dal riquadro.



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
<li>Informazioni sull'autorità di attendibilità di input e output per i nodi Transform e output.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Input nodo</td>
<td><ul>
<li><a href="media-type-attributes.md">Attributi del tipo di supporto</a> per tutti i nodi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Output del nodo</td>
<td><ul>
<li><a href="stream-descriptor-attributes.md">Attributi del descrittore di flusso</a> solo per i nodi di origine.<br/></li>
<li><a href="media-type-attributes.md">Attributi del tipo di supporto</a> per tutti i nodi.<br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

È possibile modificare i valori degli attributi, ad eccezione dei riferimenti ai puntatori e dei valori di matrice. Per modificare un valore di attributo, digitare il nuovo valore accanto all'attributo e fare clic su **Salva** nel **riquadro attributi**. Il nuovo valore viene aggiornato nell'archivio attributi e applicato alla topologia solo dopo che è stato risolto.

## <a name="to-add-a-new-attribute-for-a-node"></a>Per aggiungere un nuovo attributo per un nodo

1.  Selezionare il nodo facendo clic su di esso nel **riquadro topologia**.

    Gli attributi impostati nel nodo vengono visualizzati nel **riquadro attributi**.

2.  Nel **riquadro attributi** fare clic su **Aggiungi**.

    Verrà visualizzata la finestra di dialogo **Aggiungi attributo** .

3.  Dal primo elenco a discesa, scegliere la categoria attributo.

    Le categorie dipendono dal nodo della topologia. Per il nodo di origine, ad esempio, l'elenco a discesa Mostra gli **attributi del descrittore di presentazione** e **gli attributi del nodo** come categorie disponibili.

4.  Nel secondo elenco a discesa scegliere l'attributo che si desidera impostare nel nodo.

5.  Nella casella di modifica aggiungere il valore per l'attributo.

6.  Fare clic su **Aggiungi** per aggiungere l'attributo e tornare alla finestra principale oppure fare clic su **Annulla** per annullare l'operazione.

7.  Scegliere **Risolvi topologia** dal menu **topologia** per impostare il nuovo attributo sulla topologia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




