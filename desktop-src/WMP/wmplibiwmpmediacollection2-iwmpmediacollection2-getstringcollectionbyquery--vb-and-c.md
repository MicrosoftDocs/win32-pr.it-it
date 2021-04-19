---
title: Metodo IWMPMediaCollection2 getStringCollectionByQuery
description: Il metodo getStringCollectionByQuery restituisce un'interfaccia IWMPStringCollection che fornisce l'accesso al set di tutti i valori stringa per un attributo specificato che soddisfano le condizioni della query.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- Metodo getStringCollectionByQuery Windows Media Player
- Metodo getStringCollectionByQuery Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player, metodo getStringCollectionByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329063"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a><span data-ttu-id="7e0a8-106">Metodo IWMPMediaCollection2:: getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="7e0a8-106">IWMPMediaCollection2::getStringCollectionByQuery method</span></span>

<span data-ttu-id="7e0a8-107">Il `getStringCollectionByQuery` metodo restituisce un'interfaccia **IWMPStringCollection** che consente di accedere al set di tutti i valori stringa per un attributo specificato che soddisfano le condizioni della query.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-107">The `getStringCollectionByQuery` method returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e0a8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e0a8-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a><span data-ttu-id="7e0a8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e0a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e0a8-110">*bstrAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e0a8-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0a8-111">**System. String** che rappresenta il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-111">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="7e0a8-112">*pQuery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e0a8-112">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0a8-113">Interfaccia **wmplib. IWMPQuery** che rappresenta la query che definisce le condizioni utilizzate per recuperare la raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-113">The **WMPLib.IWMPQuery** interface that is the query that defines the conditions used to retrieve the string collection.</span></span>

</dd> <dt>

<span data-ttu-id="7e0a8-114">*bstrMediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e0a8-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0a8-115">**System. String** che rappresenta il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-115">The **System.String** that is the media type.</span></span> <span data-ttu-id="7e0a8-116">Deve contenere uno dei valori seguenti: "audio", "video", "Photo", "playlist" o "other".</span><span class="sxs-lookup"><span data-stu-id="7e0a8-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="7e0a8-117">*bstrSortAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e0a8-117">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0a8-118">**System. String** che rappresenta il nome dell'attributo utilizzato per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-118">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="7e0a8-119">Una stringa di lunghezza zero ("") indica che non viene applicato alcun ordinamento.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-119">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="7e0a8-120">*fSortAscending* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e0a8-120">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0a8-121">Valore **System. Boolean** che indica se il set di valori di stringa deve essere ordinato in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-121">The **System.Boolean** value that indicates whether the set of string values must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e0a8-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e0a8-122">Return value</span></span>

<span data-ttu-id="7e0a8-123">Interfaccia **wmplib. IWMPStringCollection** per il set recuperato di valori stringa.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-123">A **WMPLib.IWMPStringCollection** interface for the retrieved set of string values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e0a8-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e0a8-124">Remarks</span></span>

<span data-ttu-id="7e0a8-125">Le query composte con **IWMPQuery** non fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="7e0a8-125">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="7e0a8-126">Quando la query composta specificata dal parametro *pQuery* contiene una condizione compilata sull'attributo **mediaType** , tale condizione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-126">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="7e0a8-127">Viene sempre usato il valore per il parametro *bstrMediaType* .</span><span class="sxs-lookup"><span data-stu-id="7e0a8-127">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="7e0a8-128">Se, ad esempio, la query composta contiene la condizione "MediaType Equals audio" e il valore per il parametro *bstrMediaType* è "video", la playlist risultante conterrà solo elementi video.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e0a8-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e0a8-129">Requirements</span></span>



| <span data-ttu-id="7e0a8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e0a8-130">Requirement</span></span> | <span data-ttu-id="7e0a8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="7e0a8-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0a8-132">Versione</span><span class="sxs-lookup"><span data-stu-id="7e0a8-132">Version</span></span><br/>   | <span data-ttu-id="7e0a8-133">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="7e0a8-133">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="7e0a8-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7e0a8-134">Namespace</span></span><br/> | <span data-ttu-id="7e0a8-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7e0a8-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7e0a8-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="7e0a8-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7e0a8-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7e0a8-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e0a8-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e0a8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e0a8-139">**Interfaccia IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7e0a8-139">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e0a8-140">**Interfaccia IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7e0a8-140">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e0a8-141">**Interfaccia IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7e0a8-141">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e0a8-142">**Attributo MediaType**</span><span class="sxs-lookup"><span data-stu-id="7e0a8-142">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





