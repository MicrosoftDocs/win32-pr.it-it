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
# <a name="viewing-topology-information"></a><span data-ttu-id="7b63e-103">Visualizzazione delle informazioni sulla topologia</span><span class="sxs-lookup"><span data-stu-id="7b63e-103">Viewing Topology Information</span></span>

<span data-ttu-id="7b63e-104">In TopoEdit, a ogni elemento della topologia, ad esempio nodi, input del nodo e output del nodo, è associato un archivio attributi che gestisce il comportamento del nodo.</span><span class="sxs-lookup"><span data-stu-id="7b63e-104">In TopoEdit, each topology item, such as nodes, node inputs, and node outputs, has an associated attribute store that manages the behavior of the node.</span></span> <span data-ttu-id="7b63e-105">Per visualizzare gli attributi, selezionare l'elemento e nel **riquadro attributi** vengono visualizzate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7b63e-105">To see the attributes, select the item, and the **Attributes Pane** displays the information.</span></span> <span data-ttu-id="7b63e-106">Per le topologie caricate da un file XML, è possibile che alcuni nodi non visualizzino l'intero archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="7b63e-106">For topologies that are loaded from an XML file, some of the nodes may not display the entire attribute store.</span></span> <span data-ttu-id="7b63e-107">Per visualizzare l'intero archivio attributi, risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="7b63e-107">To see the entire attribute store, resolve the topology.</span></span> <span data-ttu-id="7b63e-108">Per ulteriori informazioni, vedere la pagina relativa alla [risoluzione di una topologia con TopoEdit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="7b63e-108">For more information, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="7b63e-109">Nella tabella seguente vengono illustrati l'elemento della topologia e gli attributi visualizzati dal riquadro.</span><span class="sxs-lookup"><span data-stu-id="7b63e-109">The following table shows the topology item and the attributes that the pane displays.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b63e-110">Elemento topologia</span><span class="sxs-lookup"><span data-stu-id="7b63e-110">Topology item</span></span></th>
<th><span data-ttu-id="7b63e-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="7b63e-111">Attributes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b63e-112">Nodi della topologia</span><span class="sxs-lookup"><span data-stu-id="7b63e-112">Topology nodes</span></span></td>
<td><ul>
<li><span data-ttu-id="7b63e-113"><a href="topology-node-attributes.md">Attributi del nodo della topologia</a> per tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="7b63e-113"><a href="topology-node-attributes.md">Topology Node Attributes</a> for all nodes.</span></span><br/></li>
<li><span data-ttu-id="7b63e-114"><a href="presentation-descriptor-attributes.md">Attributi del descrittore di presentazione</a> solo per i nodi di origine.</span><span class="sxs-lookup"><span data-stu-id="7b63e-114"><a href="presentation-descriptor-attributes.md">Presentation Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="7b63e-115">Informazioni sull'autorità di attendibilità di input e output per i nodi Transform e output.</span><span class="sxs-lookup"><span data-stu-id="7b63e-115">Input and output trust authority information for transform and output nodes.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b63e-116">Input nodo</span><span class="sxs-lookup"><span data-stu-id="7b63e-116">Node input</span></span></td>
<td><ul>
<li><span data-ttu-id="7b63e-117"><a href="media-type-attributes.md">Attributi del tipo di supporto</a> per tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="7b63e-117"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b63e-118">Output del nodo</span><span class="sxs-lookup"><span data-stu-id="7b63e-118">Node output</span></span></td>
<td><ul>
<li><span data-ttu-id="7b63e-119"><a href="stream-descriptor-attributes.md">Attributi del descrittore di flusso</a> solo per i nodi di origine.</span><span class="sxs-lookup"><span data-stu-id="7b63e-119"><a href="stream-descriptor-attributes.md">Stream Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="7b63e-120"><a href="media-type-attributes.md">Attributi del tipo di supporto</a> per tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="7b63e-120"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span><br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7b63e-121">È possibile modificare i valori degli attributi, ad eccezione dei riferimenti ai puntatori e dei valori di matrice.</span><span class="sxs-lookup"><span data-stu-id="7b63e-121">The attribute values, except for pointer references and array values, can be changed.</span></span> <span data-ttu-id="7b63e-122">Per modificare un valore di attributo, digitare il nuovo valore accanto all'attributo e fare clic su **Salva** nel **riquadro attributi**.</span><span class="sxs-lookup"><span data-stu-id="7b63e-122">To change an attribute value, type in the new value next to the attribute and click **Save** on the **Attributes Pane**.</span></span> <span data-ttu-id="7b63e-123">Il nuovo valore viene aggiornato nell'archivio attributi e applicato alla topologia solo dopo che è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="7b63e-123">The new value is updated in the attribute store and applied to the topology only after it is resolved.</span></span>

## <a name="to-add-a-new-attribute-for-a-node"></a><span data-ttu-id="7b63e-124">Per aggiungere un nuovo attributo per un nodo</span><span class="sxs-lookup"><span data-stu-id="7b63e-124">To add a new attribute for a node</span></span>

1.  <span data-ttu-id="7b63e-125">Selezionare il nodo facendo clic su di esso nel **riquadro topologia**.</span><span class="sxs-lookup"><span data-stu-id="7b63e-125">Select the node by clicking it on the **Topology Pane**.</span></span>

    <span data-ttu-id="7b63e-126">Gli attributi impostati nel nodo vengono visualizzati nel **riquadro attributi**.</span><span class="sxs-lookup"><span data-stu-id="7b63e-126">The attributes that are set on the node are shown on the **Attributes Pane**.</span></span>

2.  <span data-ttu-id="7b63e-127">Nel **riquadro attributi** fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="7b63e-127">On the **Attributes Pane**, click **Add**.</span></span>

    <span data-ttu-id="7b63e-128">Verrà visualizzata la finestra di dialogo **Aggiungi attributo** .</span><span class="sxs-lookup"><span data-stu-id="7b63e-128">This opens the **Add Attribute** dialog box.</span></span>

3.  <span data-ttu-id="7b63e-129">Dal primo elenco a discesa, scegliere la categoria attributo.</span><span class="sxs-lookup"><span data-stu-id="7b63e-129">From the first drop-down list, choose the Attribute category.</span></span>

    <span data-ttu-id="7b63e-130">Le categorie dipendono dal nodo della topologia.</span><span class="sxs-lookup"><span data-stu-id="7b63e-130">The categories depend on the topology node.</span></span> <span data-ttu-id="7b63e-131">Per il nodo di origine, ad esempio, l'elenco a discesa Mostra gli **attributi del descrittore di presentazione** e **gli attributi del nodo** come categorie disponibili.</span><span class="sxs-lookup"><span data-stu-id="7b63e-131">For example, for the source node, the drop-down list shows **Presentation Descriptor Attributes** and **Node Attributes** as the available categories.</span></span>

4.  <span data-ttu-id="7b63e-132">Nel secondo elenco a discesa scegliere l'attributo che si desidera impostare nel nodo.</span><span class="sxs-lookup"><span data-stu-id="7b63e-132">From the second drop-down list, choose the attribute that you want to set on the node.</span></span>

5.  <span data-ttu-id="7b63e-133">Nella casella di modifica aggiungere il valore per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="7b63e-133">In the edit box, add the value for the attribute.</span></span>

6.  <span data-ttu-id="7b63e-134">Fare clic su **Aggiungi** per aggiungere l'attributo e tornare alla finestra principale oppure fare clic su **Annulla** per annullare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7b63e-134">Click **Add** to add the attribute and return to the main window, or click **Cancel** to cancel the operation.</span></span>

7.  <span data-ttu-id="7b63e-135">Scegliere **Risolvi topologia** dal menu **topologia** per impostare il nuovo attributo sulla topologia.</span><span class="sxs-lookup"><span data-stu-id="7b63e-135">From the **Topology** menu, click **Resolve Topology** to set the new attribute to the topology.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b63e-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b63e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b63e-137">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="7b63e-137">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




