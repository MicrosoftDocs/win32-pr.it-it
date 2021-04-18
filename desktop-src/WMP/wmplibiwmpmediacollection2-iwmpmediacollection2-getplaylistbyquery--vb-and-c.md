---
title: Metodo IWMPMediaCollection2 getPlaylistByQuery
description: Il metodo getPlaylistByQuery restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali che soddisfano le condizioni della query.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- Metodo getPlaylistByQuery Windows Media Player
- Metodo getPlaylistByQuery Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player, metodo getPlaylistByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329064"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a><span data-ttu-id="c2e6c-106">Metodo IWMPMediaCollection2:: getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="c2e6c-106">IWMPMediaCollection2::getPlaylistByQuery method</span></span>

<span data-ttu-id="c2e6c-107">Il `getPlaylistByQuery` metodo restituisce un'interfaccia **IWMPPlaylist** che consente di accedere agli elementi multimediali che corrispondono alle condizioni della query.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-107">The `getPlaylistByQuery` method returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e6c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2e6c-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a><span data-ttu-id="c2e6c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2e6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e6c-110">*pQuery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2e6c-110">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e6c-111">Interfaccia **wmplib. IWMPQuery** che rappresenta la query.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-111">The **WMPLib.IWMPQuery** interface that represents the query.</span></span>

</dd> <dt>

<span data-ttu-id="c2e6c-112">*bstrMediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2e6c-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e6c-113">**System. String** che rappresenta il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-113">The **System.String** that is the media type.</span></span> <span data-ttu-id="c2e6c-114">Deve contenere uno dei valori seguenti: "audio", "video", "Photo", "playlist" o "other".</span><span class="sxs-lookup"><span data-stu-id="c2e6c-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="c2e6c-115">*bstrSortAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2e6c-115">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e6c-116">**System. String** che rappresenta il nome dell'attributo utilizzato per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-116">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="c2e6c-117">Una stringa di lunghezza zero ("") indica che non viene applicato alcun ordinamento.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-117">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="c2e6c-118">*fSortAscending* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2e6c-118">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e6c-119">Valore **System. Boolean** che indica se la playlist deve essere ordinata in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-119">The **System.Boolean** value that indicates whether the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e6c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2e6c-120">Return value</span></span>

<span data-ttu-id="c2e6c-121">Interfaccia **wmplib. IWMPPlaylist** per la playlist recuperata.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-121">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e6c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2e6c-122">Remarks</span></span>

<span data-ttu-id="c2e6c-123">Le query composte con **IWMPQuery** non fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="c2e6c-123">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="c2e6c-124">Quando la query composta specificata dal parametro *pQuery* contiene una condizione compilata sull'attributo **mediaType** , tale condizione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-124">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="c2e6c-125">Viene sempre usato il valore per il parametro *bstrMediaType* .</span><span class="sxs-lookup"><span data-stu-id="c2e6c-125">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="c2e6c-126">Se, ad esempio, la query composta contiene la condizione "MediaType Equals audio" e il valore per il parametro *bstrMediaType* è "video", la playlist risultante conterrà solo elementi video.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e6c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2e6c-127">Requirements</span></span>



| <span data-ttu-id="c2e6c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e6c-128">Requirement</span></span> | <span data-ttu-id="c2e6c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c2e6c-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e6c-130">Versione</span><span class="sxs-lookup"><span data-stu-id="c2e6c-130">Version</span></span><br/>   | <span data-ttu-id="c2e6c-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="c2e6c-131">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="c2e6c-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c2e6c-132">Namespace</span></span><br/> | <span data-ttu-id="c2e6c-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c2e6c-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c2e6c-134">Assembly</span><span class="sxs-lookup"><span data-stu-id="c2e6c-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c2e6c-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e6c-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e6c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2e6c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e6c-137">**Interfaccia IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c2e6c-137">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2e6c-138">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c2e6c-138">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2e6c-139">**Interfaccia IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c2e6c-139">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2e6c-140">**Attributo MediaType**</span><span class="sxs-lookup"><span data-stu-id="c2e6c-140">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





