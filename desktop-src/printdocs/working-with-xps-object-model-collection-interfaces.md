---
description: Viene descritto come utilizzare i metodi comuni delle interfacce di raccolta.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Uso delle interfacce di raccolta OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232134"
---
# <a name="working-with-xps-om-collection-interfaces"></a><span data-ttu-id="5eb17-103">Uso delle interfacce di raccolta OM XPS</span><span class="sxs-lookup"><span data-stu-id="5eb17-103">Working with XPS OM Collection Interfaces</span></span>

<span data-ttu-id="5eb17-104">Viene descritto come utilizzare i metodi comuni delle interfacce di raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-104">Describes how to use the common methods of the collection interfaces.</span></span>

## <a name="contents"></a><span data-ttu-id="5eb17-105">Contenuto</span><span class="sxs-lookup"><span data-stu-id="5eb17-105">Contents</span></span>

<span data-ttu-id="5eb17-106">I metodi descritti in questa sezione sono illustrati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="5eb17-106">The methods described in this section are shown in the list that follows.</span></span> <span data-ttu-id="5eb17-107">Non tutte le interfacce di raccolta supportano ognuno di questi metodi e alcune interfacce supportano anche metodi non descritti in questa pagina.</span><span class="sxs-lookup"><span data-stu-id="5eb17-107">Not all collection interfaces support each of these methods, and some interfaces also support methods that are not described on this page.</span></span> <span data-ttu-id="5eb17-108">Per l'elenco dei metodi supportati da un'interfaccia specifica, fare riferimento alla descrizione della descrizione di tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5eb17-108">For the list of methods supported by a specific interface, refer to the description of that interface's description.</span></span>

<dl>

[<span data-ttu-id="5eb17-109">Append (metodo)</span><span class="sxs-lookup"><span data-stu-id="5eb17-109">Append Method</span></span>](#append-method)  
[<span data-ttu-id="5eb17-110">Metodo GetAt</span><span class="sxs-lookup"><span data-stu-id="5eb17-110">GetAt Method</span></span>](#getat-method)  
[<span data-ttu-id="5eb17-111">Metodo GetCount</span><span class="sxs-lookup"><span data-stu-id="5eb17-111">GetCount Method</span></span>](#getcount-method)  
[<span data-ttu-id="5eb17-112">Metodo InsertAt</span><span class="sxs-lookup"><span data-stu-id="5eb17-112">InsertAt Method</span></span>](#insertat-method)  
[<span data-ttu-id="5eb17-113">RemoveAt (metodo)</span><span class="sxs-lookup"><span data-stu-id="5eb17-113">RemoveAt Method</span></span>](#removeat-method)  
[<span data-ttu-id="5eb17-114">Metodo SetAt</span><span class="sxs-lookup"><span data-stu-id="5eb17-114">SetAt Method</span></span>](#setat-method)  
</dl>

[<span data-ttu-id="5eb17-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5eb17-115">See also</span></span>](#see-also)

## <a name="append-method"></a><span data-ttu-id="5eb17-116">Append (metodo)</span><span class="sxs-lookup"><span data-stu-id="5eb17-116">Append Method</span></span>

<span data-ttu-id="5eb17-117">Accoda un oggetto alla fine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-117">Appends an object to the end of the collection.</span></span>

<span data-ttu-id="5eb17-118">**Sintassi generica**</span><span class="sxs-lookup"><span data-stu-id="5eb17-118">**Generic Syntax**</span></span>


```C++
HRESULT Append(
  [in]  Object *object
);
```



<span data-ttu-id="5eb17-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5eb17-119">**Description**</span></span>

<span data-ttu-id="5eb17-120">Alla fine della raccolta, questo metodo aggiunge un oggetto che viene passato nell'elenco di parametri, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="5eb17-120">To the end of the collection, this method appends an object that is passed in the parameter list, as shown in the following diagram.</span></span>

![figura che Mostra come accodare aggiunge una voce alla raccolta](images/generic-append.png)

## <a name="getat-method"></a><span data-ttu-id="5eb17-122">Metodo GetAt</span><span class="sxs-lookup"><span data-stu-id="5eb17-122">GetAt Method</span></span>

<span data-ttu-id="5eb17-123">Ottiene un oggetto da una posizione specificata nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-123">Gets an object from a specified location in the collection.</span></span>

<span data-ttu-id="5eb17-124">**Sintassi generica**</span><span class="sxs-lookup"><span data-stu-id="5eb17-124">**Generic Syntax**</span></span>


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



<span data-ttu-id="5eb17-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5eb17-125">**Description**</span></span>

<span data-ttu-id="5eb17-126">Scrive l'oggetto archiviato nel percorso della raccolta specificato dall' *Indice* nella variabile a cui fa riferimento l' *oggetto*.</span><span class="sxs-lookup"><span data-stu-id="5eb17-126">Writes the object that is stored at the collection's location specified by *index* to the variable referenced by *object*.</span></span> <span data-ttu-id="5eb17-127">Questa azione non modifica il contenuto della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-127">This action does not change the collection's contents.</span></span> <span data-ttu-id="5eb17-128">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="5eb17-128">The following diagram illustrates this process.</span></span>

![una figura che Mostra come il metodo Geta recupera una voce dalla raccolta](images/generic-getat.png)

## <a name="getcount-method"></a><span data-ttu-id="5eb17-130">Metodo GetCount</span><span class="sxs-lookup"><span data-stu-id="5eb17-130">GetCount Method</span></span>

<span data-ttu-id="5eb17-131">Ottiene il numero di oggetti archiviati nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-131">Gets the number of objects stored in the collection.</span></span>

<span data-ttu-id="5eb17-132">**Sintassi generica**</span><span class="sxs-lookup"><span data-stu-id="5eb17-132">**Generic Syntax**</span></span>


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



<span data-ttu-id="5eb17-133">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5eb17-133">**Description**</span></span>

<span data-ttu-id="5eb17-134">Scrive il numero di oggetti attualmente archiviati nella raccolta nella variabile a cui fa riferimento *count*.</span><span class="sxs-lookup"><span data-stu-id="5eb17-134">Writes the number of objects that are currently stored in the collection into the variable referenced by *count*.</span></span> <span data-ttu-id="5eb17-135">Questa azione non modifica il contenuto della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-135">This action does not change the collection's contents.</span></span> <span data-ttu-id="5eb17-136">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="5eb17-136">The following diagram illustrates this process.</span></span>

![figura che mostra il modo in cui GetCount ottiene il numero di voci nella raccolta](images/generic-getcount.png)

## <a name="insertat-method"></a><span data-ttu-id="5eb17-138">Metodo InsertAt</span><span class="sxs-lookup"><span data-stu-id="5eb17-138">InsertAt Method</span></span>

<span data-ttu-id="5eb17-139">Inserisce un oggetto in una posizione specificata della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-139">Inserts an object at a specified location of the collection.</span></span>

<span data-ttu-id="5eb17-140">**Sintassi generica**</span><span class="sxs-lookup"><span data-stu-id="5eb17-140">**Generic Syntax**</span></span>


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="5eb17-141">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5eb17-141">**Description**</span></span>

<span data-ttu-id="5eb17-142">L'oggetto passato nell' *oggetto* viene inserito nella raccolta in corrispondenza della posizione specificata da *index*.</span><span class="sxs-lookup"><span data-stu-id="5eb17-142">The object that is passed in *object* is inserted into the collection at the location specified by *index*.</span></span> <span data-ttu-id="5eb17-143">Prima di inserire il nuovo *oggetto*, questo metodo viene spostato di 1 nell'oggetto che in precedenza occupava la posizione in corrispondenza dell' *Indice* e sposta tutti i puntatori di interfaccia successivi a *index*.</span><span class="sxs-lookup"><span data-stu-id="5eb17-143">Before inserting the new *object*, this method moves by 1 the object that has previously occupied the location at *index* and moves all interface pointers subsequent to *index*.</span></span> <span data-ttu-id="5eb17-144">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="5eb17-144">The following diagram illustrates this process.</span></span>

![figura che Mostra come InsertAt aggiunge una voce alla raccolta](images/generic-insertat.png)

## <a name="removeat-method"></a><span data-ttu-id="5eb17-146">RemoveAt (metodo)</span><span class="sxs-lookup"><span data-stu-id="5eb17-146">RemoveAt Method</span></span>

<span data-ttu-id="5eb17-147">Rimuove l'oggetto da una posizione specificata nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-147">Removes the object from a specified location in the collection.</span></span>

<span data-ttu-id="5eb17-148">**Sintassi generica**</span><span class="sxs-lookup"><span data-stu-id="5eb17-148">**Generic Syntax**</span></span>


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



<span data-ttu-id="5eb17-149">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5eb17-149">**Description**</span></span>

<span data-ttu-id="5eb17-150">Questo metodo rilascia l'oggetto dalla posizione specificata da *index*, quindi compatta la raccolta riducendo di 1 l'indice di ogni puntatore successivo a *index*.</span><span class="sxs-lookup"><span data-stu-id="5eb17-150">This method releases the object from the location specified by *index*, then compacts the collection by reducing by 1 the index of each pointer subsequent to *index*.</span></span> <span data-ttu-id="5eb17-151">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="5eb17-151">The following diagram illustrates this process.</span></span>

![figura che illustra in che modo RemoveAt rimuove una voce dalla raccolta](images/generic-removeat.png)

## <a name="setat-method"></a><span data-ttu-id="5eb17-153">Metodo SetAt</span><span class="sxs-lookup"><span data-stu-id="5eb17-153">SetAt Method</span></span>

<span data-ttu-id="5eb17-154">Sostituisce l'oggetto in una posizione specificata nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5eb17-154">Replaces the object at a specified location in the collection.</span></span>

<span data-ttu-id="5eb17-155">**Sintassi generica**</span><span class="sxs-lookup"><span data-stu-id="5eb17-155">**Generic Syntax**</span></span>


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="5eb17-156">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5eb17-156">**Description**</span></span>

<span data-ttu-id="5eb17-157">Questo metodo prima rilascia l'oggetto in corrispondenza della posizione a cui fa riferimento *index*, quindi sostituisce tale oggetto con quello passato all' *oggetto*.</span><span class="sxs-lookup"><span data-stu-id="5eb17-157">This method first releases the object at the location referenced by *index*, then replaces that object with the one that is passed in *object*.</span></span> <span data-ttu-id="5eb17-158">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="5eb17-158">The following diagram illustrates this process.</span></span>

![figura che Mostra come SetAt sostituisce una voce nella raccolta](images/generic-setat.png)

## <a name="see-also"></a><span data-ttu-id="5eb17-160">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5eb17-160">See Also</span></span>

<dl>

[<span data-ttu-id="5eb17-161">**IXpsOMColorProfileResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-161">**IXpsOMColorProfileResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[<span data-ttu-id="5eb17-162">**IXpsOMDashCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-162">**IXpsOMDashCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[<span data-ttu-id="5eb17-163">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-163">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[<span data-ttu-id="5eb17-164">**IXpsOMFontResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-164">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[<span data-ttu-id="5eb17-165">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-165">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[<span data-ttu-id="5eb17-166">**IXpsOMGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-166">**IXpsOMGradientStopCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[<span data-ttu-id="5eb17-167">**IXpsOMImageResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-167">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[<span data-ttu-id="5eb17-168">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-168">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[<span data-ttu-id="5eb17-169">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-169">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[<span data-ttu-id="5eb17-170">**IXpsOMPartUriCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-170">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[<span data-ttu-id="5eb17-171">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-171">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[<span data-ttu-id="5eb17-172">**IXpsOMSignatureBlockResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-172">**IXpsOMSignatureBlockResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[<span data-ttu-id="5eb17-173">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-173">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[<span data-ttu-id="5eb17-174">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-174">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[<span data-ttu-id="5eb17-175">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-175">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[<span data-ttu-id="5eb17-176">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="5eb17-176">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



