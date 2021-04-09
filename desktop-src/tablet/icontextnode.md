---
description: Rappresenta un nodo in un albero di oggetti creati come parte dell'analisi dell'input penna.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Interfaccia IContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049519"
---
# <a name="icontextnode-interface"></a><span data-ttu-id="f7ee3-103">Interfaccia IContextNode</span><span class="sxs-lookup"><span data-stu-id="f7ee3-103">IContextNode interface</span></span>

<span data-ttu-id="f7ee3-104">Rappresenta un nodo in un albero di oggetti creati come parte dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-104">Represents a node in a tree of objects that are created as part of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="f7ee3-105">Membri</span><span class="sxs-lookup"><span data-stu-id="f7ee3-105">Members</span></span>

<span data-ttu-id="f7ee3-106">L'interfaccia **IContextNode** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-106">The **IContextNode** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f7ee3-107">**IContextNode** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f7ee3-107">**IContextNode** also has these types of members:</span></span>

-   [<span data-ttu-id="f7ee3-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="f7ee3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f7ee3-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f7ee3-109">Methods</span></span>

<span data-ttu-id="f7ee3-110">L'interfaccia **IContextNode** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-110">The **IContextNode** interface has these methods.</span></span>



| <span data-ttu-id="f7ee3-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="f7ee3-111">Method</span></span>                                                                                  | <span data-ttu-id="f7ee3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7ee3-112">Description</span></span>                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7ee3-113">**AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-113">**AddContextLink**</span></span>](icontextnode-addcontextlink.md)                                   | <span data-ttu-id="f7ee3-114">Aggiunge un nuovo [**IContextLink**](icontextlink.md) alla raccolta di collegamenti di contesto dell'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-114">Adds a new [**IContextLink**](icontextlink.md) to the **IContextNode** object's context link collection.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="f7ee3-115">**AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-115">**AddPropertyData**</span></span>](icontextnode-addpropertydata.md)                                 | <span data-ttu-id="f7ee3-116">Aggiunge un elemento di dati specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-116">Adds a piece of application-specific data.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="f7ee3-117">**Confermare**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-117">**Confirm**</span></span>](icontextnode-confirm.md)                                                 | <span data-ttu-id="f7ee3-118">Modifica il tipo di conferma, che consente di controllare le modifiche apportate all'oggetto [**IInkAnalyzer**](iinkanalyzer.md) in **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-118">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the **IContextNode**.</span></span><br/>                                                                         |
| [<span data-ttu-id="f7ee3-119">**ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-119">**ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)                       | <span data-ttu-id="f7ee3-120">Determina se l'oggetto **IContextNode** contiene dati archiviati con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-120">Determines whether the **IContextNode** object contains data stored under the specified identifier.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="f7ee3-121">**CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-121">**CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md) | <span data-ttu-id="f7ee3-122">Crea un oggetto **IContextNode** figlio contenente solo le informazioni sul tipo, sull'identificatore e sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-122">Creates a child **IContextNode** object that contains only information on type, identifier, and location.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="f7ee3-123">**CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-123">**CreateSubNode**</span></span>](icontextnode-createsubnode.md)                                     | <span data-ttu-id="f7ee3-124">Crea un nuovo oggetto **IContextNode** figlio.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-124">Creates a new child **IContextNode** object.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="f7ee3-125">**DeleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-125">**DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)                             | <span data-ttu-id="f7ee3-126">Elimina un oggetto [**IContextLink**](icontextlink.md) dalla raccolta di collegamenti dell'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-126">Deletes an [**IContextLink**](icontextlink.md) object from the **IContextNode** object's link collection.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="f7ee3-127">**DeleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-127">**DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)                                     | <span data-ttu-id="f7ee3-128">Rimuove un **IContextNode** figlio.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-128">Removes a child **IContextNode**.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="f7ee3-129">**GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-129">**GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)                                 | <span data-ttu-id="f7ee3-130">Recupera una raccolta di oggetti [**IContextLink**](icontextlink.md) che rappresenta relazioni con altri oggetti **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-130">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other **IContextNode** objects.</span></span><br/>                                                                          |
| [<span data-ttu-id="f7ee3-131">**GetId**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-131">**GetId**</span></span>](icontextnode-getid.md)                                                     | <span data-ttu-id="f7ee3-132">Recupera l'identificatore per l'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-132">Retrieves the identifier for the **IContextNode** object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="f7ee3-133">**GetLocation**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-133">**GetLocation**</span></span>](icontextnode-getlocation.md)                                         | <span data-ttu-id="f7ee3-134">Recupera la posizione e le dimensioni dell'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-134">Retrieves the position and size of the **IContextNode** object.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="f7ee3-135">**GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-135">**GetParentNode**</span></span>](icontextnode-getparentnode.md)                                     | <span data-ttu-id="f7ee3-136">Recupera il nodo padre di questo **IContextNode** nell'albero del nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-136">Retrieves the parent node of this **IContextNode** in the context node tree.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="f7ee3-137">**GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-137">**GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)                     | <span data-ttu-id="f7ee3-138">Recupera il valore che indica se un oggetto **IContextNode** è parzialmente popolato o completamente popolato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-138">Retrieves the value that indicates whether an **IContextNode** object is partially populated or fully populated.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="f7ee3-139">**GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-139">**GetPropertyData**</span></span>](icontextnode-getpropertydata.md)                                 | <span data-ttu-id="f7ee3-140">Recupera dati specifici dell'applicazione o altri dati della proprietà in base all'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-140">Retrieves application-specific data or other property data given the specified identifier.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="f7ee3-141">**GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-141">**GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)                           | <span data-ttu-id="f7ee3-142">Recupera gli identificatori per i quali sono presenti dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-142">Retrieves the identifiers for which there is property data.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="f7ee3-143">**GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-143">**GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)                                   | <span data-ttu-id="f7ee3-144">Recupera il numero di tratti associati all'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-144">Retrieves the number of strokes associated with the **IContextNode** object.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="f7ee3-145">**GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-145">**GetStrokeId**</span></span>](icontextnode-getstrokeid.md)                                         | <span data-ttu-id="f7ee3-146">Recupera l'identificatore del tratto per il tratto a cui fa riferimento un valore di indice all'interno dell'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-146">Retrieves the stroke identifier for the stroke referenced by an index value within the **IContextNode** object.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="f7ee3-147">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-147">**GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)                                       | <span data-ttu-id="f7ee3-148">Recupera una matrice di identificatori per i tratti all'interno dell'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-148">Retrieves an array of identifiers for the strokes within the **IContextNode** object.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="f7ee3-149">**GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-149">**GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)                 | <span data-ttu-id="f7ee3-150">Recupera una matrice contenente i dati della proprietà del pacchetto per il tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-150">Retrieves an array containing the packet property data for the specified stroke.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="f7ee3-151">**GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-151">**GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)   | <span data-ttu-id="f7ee3-152">Recupera una matrice contenente gli identificatori di proprietà del pacchetto per il tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-152">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="f7ee3-153">**GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-153">**GetSubNodes**</span></span>](icontextnode-getsubnodes.md)                                         | <span data-ttu-id="f7ee3-154">Recupera i nodi figlio diretti dell'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-154">Retrieves the direct child nodes of the **IContextNode** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="f7ee3-155">**GetType**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-155">**GetType**</span></span>](icontextnode-gettype.md)                                                 | <span data-ttu-id="f7ee3-156">Recupera il tipo dell'oggetto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-156">Retrieves the type of the **IContextNode** object.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="f7ee3-157">**GetTypeName**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-157">**GetTypeName**</span></span>](icontextnode-gettypename.md)                                         | <span data-ttu-id="f7ee3-158">Recupera un nome di tipo leggibile di questo **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-158">Retrieves a human-readable type name of this **IContextNode**.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="f7ee3-159">**IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-159">**IsConfirmed**</span></span>](icontextnode-isconfirmed.md)                                         | <span data-ttu-id="f7ee3-160">Recupera un valore che indica se l'oggetto **IContextNode** è confermato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-160">Retrieves a value that indicates whether the **IContextNode** object is confirmed.</span></span> <span data-ttu-id="f7ee3-161">[**IInkAnalyzer**](iinkanalyzer.md) non è in grado di modificare il tipo di nodo e i tratti associati per gli oggetti **IContextNode** confermati.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-161">[**IInkAnalyzer**](iinkanalyzer.md) cannot change the node type and associated strokes for confirmed **IContextNode** objects.</span></span><br/> |
| [<span data-ttu-id="f7ee3-162">**LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-162">**LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)                           | <span data-ttu-id="f7ee3-163">Ricrea i dati delle proprietà specifiche dell'applicazione e interni per una matrice di byte creata in precedenza con [**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="f7ee3-163">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span><br/>                  |
| [<span data-ttu-id="f7ee3-164">**MoveSubNodeToPosition**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-164">**MoveSubNodeToPosition**</span></span>](icontextnode-movesubnodetoposition.md)                     | <span data-ttu-id="f7ee3-165">Riordina un oggetto **IContextNode** figlio specificato nell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-165">Reorders a specified child **IContextNode** object to the specified index.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="f7ee3-166">**RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-166">**RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)                           | <span data-ttu-id="f7ee3-167">Rimuove una parte di dati specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-167">Removes a piece of application-specific data.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="f7ee3-168">**Reparent**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-168">**Reparent**</span></span>](icontextnode-reparent.md)                                               | <span data-ttu-id="f7ee3-169">Sposta questo oggetto **IContextNode** dalla raccolta dei sottonodi del nodo di contesto padre alla raccolta di sottonodi del nodo di contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-169">Moves this **IContextNode** object from its parent context node's subnodes collection to the specified context node's subnodes collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="f7ee3-170">**ReparentStrokeByIdToNode**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-170">**ReparentStrokeByIdToNode**</span></span>](icontextnode-reparentstrokebyidtonode.md)               | <span data-ttu-id="f7ee3-171">Sposta i dati del tratto da questo **IContextNode** al **IContextNode** specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-171">Moves stroke data from this **IContextNode** to the specified **IContextNode**.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="f7ee3-172">**SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-172">**SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)                           | <span data-ttu-id="f7ee3-173">Recupera una matrice di byte che contiene i dati della proprietà interna e specifici dell'applicazione per questo **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-173">Retrieves an array of bytes that contains the application-specific and internal property data for this **IContextNode**.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f7ee3-174">**SetLocation**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-174">**SetLocation**</span></span>](icontextnode-setlocation.md)                                         | <span data-ttu-id="f7ee3-175">Aggiorna la posizione e le dimensioni di questo **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-175">Updates the position and size of this **IContextNode**.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="f7ee3-176">**SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-176">**SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)                     | <span data-ttu-id="f7ee3-177">Modifica il valore che indica se questo **IContextNode** è parzialmente o completamente popolato.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-177">Modifies the value that indicates whether this **IContextNode** is partially or fully populated.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="f7ee3-178">**SetStrokes**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-178">**SetStrokes**</span></span>](icontextnode-setstrokes.md)                                           | <span data-ttu-id="f7ee3-179">Associa i tratti specificati a questo **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-179">Associates the specified strokes with this **IContextNode**.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f7ee3-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7ee3-180">Remarks</span></span>

<span data-ttu-id="f7ee3-181">I tipi di nodi sono descritti nelle costanti dei [tipi di nodo di contesto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ee3-181">The types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="f7ee3-182">Esempio</span><span class="sxs-lookup"><span data-stu-id="f7ee3-182">Examples</span></span>

<span data-ttu-id="f7ee3-183">Nell'esempio seguente viene illustrato un metodo che esamina un **IContextNode**. il metodo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7ee3-183">The following example shows a method that examines an **IContextNode**; the method does the following:</span></span>

-   <span data-ttu-id="f7ee3-184">Ottiene il tipo del nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-184">Gets the context node's type.</span></span> <span data-ttu-id="f7ee3-185">Se il nodo di contesto è un input penna non classificato, un hint di analisi o un nodo di riconoscimento personalizzato, viene chiamato un metodo helper per esaminare le proprietà specifiche del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-185">If the context node is an unclassified ink, analysis hint, or custom recognizer node, it calls a helper method to examine specific properties of the node type.</span></span>
-   <span data-ttu-id="f7ee3-186">Se il nodo include sottonodi, esamina ogni sottonodo chiamando se stesso.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-186">If the node has subnodes, it examines each subnode by calling itself.</span></span>
-   <span data-ttu-id="f7ee3-187">Se il nodo è un nodo foglia input penna, esamina i dati del tratto per il nodo chiamando un metodo helper.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-187">If the node is an ink leaf node, it examines the stroke data for the node by calling a helper method.</span></span>

<span data-ttu-id="f7ee3-188">L'API InkAnalysis di la consente di creare un nodo di linea contenente parole di input penna e parole di testo.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-188">Ihe InkAnalysis API allows you to create a line node that contains ink words and text words.</span></span> <span data-ttu-id="f7ee3-189">Tuttavia, il parser ignorerà questi nodi misti e li considererà come nodi esterni.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-189">However, the parser will ignore these mixed nodes and will treat them like foreign nodes.</span></span> <span data-ttu-id="f7ee3-190">Questa operazione avrà effetto sull'accuratezza dell'analisi del rilevamento delle annotazioni Ink quando l'utente finale scrive in o intorno a questo nodo misto.</span><span class="sxs-lookup"><span data-stu-id="f7ee3-190">This will have impact the parsing accuracy of detecting ink annotations when the end user writes on or around this mixed node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f7ee3-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7ee3-191">Requirements</span></span>



| <span data-ttu-id="f7ee3-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7ee3-192">Requirement</span></span> | <span data-ttu-id="f7ee3-193">Valore</span><span class="sxs-lookup"><span data-stu-id="f7ee3-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ee3-194">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7ee3-194">Minimum supported client</span></span><br/> | <span data-ttu-id="f7ee3-195">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f7ee3-195">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f7ee3-196">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7ee3-196">Minimum supported server</span></span><br/> | <span data-ttu-id="f7ee3-197">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f7ee3-197">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f7ee3-198">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7ee3-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7ee3-199"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f7ee3-199"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f7ee3-200">DLL</span><span class="sxs-lookup"><span data-stu-id="f7ee3-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7ee3-201"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7ee3-201"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f7ee3-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7ee3-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ee3-203">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-203">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="f7ee3-204">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="f7ee3-204">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="f7ee3-205">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f7ee3-205">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f7ee3-206">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="f7ee3-206">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

