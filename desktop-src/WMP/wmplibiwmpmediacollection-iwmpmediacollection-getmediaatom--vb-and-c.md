---
title: Metodo IWMPMediaCollection getMediaAtom
description: Il metodo getMediaAtom restituisce l'indice di un attributo specificato all'interno del set di attributi disponibili.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- Metodo getMediaAtom Windows Media Player
- Metodo getMediaAtom Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getMediaAtom
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333404"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a><span data-ttu-id="b91e8-106">Metodo IWMPMediaCollection:: getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="b91e8-106">IWMPMediaCollection::getMediaAtom method</span></span>

<span data-ttu-id="b91e8-107">Il `getMediaAtom` metodo restituisce l'indice di un attributo specificato all'interno del set di attributi disponibili.</span><span class="sxs-lookup"><span data-stu-id="b91e8-107">The `getMediaAtom` method returns the index of a specified attribute within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91e8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b91e8-108">Syntax</span></span>


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a><span data-ttu-id="b91e8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b91e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b91e8-110">*bstrItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b91e8-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91e8-111">**System. String** che rappresenta il nome dell'elemento per il quale recuperare l'indice.</span><span class="sxs-lookup"><span data-stu-id="b91e8-111">The **System.String** that is the name of the item for which the index should be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b91e8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b91e8-112">Return value</span></span>

<span data-ttu-id="b91e8-113">**System. Int32** che rappresenta l'indice.</span><span class="sxs-lookup"><span data-stu-id="b91e8-113">The **System.Int32** that is the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="b91e8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b91e8-114">Remarks</span></span>

<span data-ttu-id="b91e8-115">Il numero di indice recuperato con questo metodo può essere passato a **IWMPMedia. getItemInfoByAtom** per accedere ai valori di attributo.</span><span class="sxs-lookup"><span data-stu-id="b91e8-115">The index number retrieved with this method can be passed to the **IWMPMedia.getItemInfoByAtom** to access attribute values.</span></span> <span data-ttu-id="b91e8-116">Questa tecnica è in genere più efficiente quando si lavora con playlist di grandi dimensioni rispetto all'accesso a un valore di attributo in base al nome tramite **IWMPMedia. GetItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="b91e8-116">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through **IWMPMedia.getItemInfo**.</span></span>

<span data-ttu-id="b91e8-117">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b91e8-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b91e8-118">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b91e8-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b91e8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b91e8-119">Requirements</span></span>



| <span data-ttu-id="b91e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b91e8-120">Requirement</span></span> | <span data-ttu-id="b91e8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b91e8-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b91e8-122">Versione</span><span class="sxs-lookup"><span data-stu-id="b91e8-122">Version</span></span><br/>   | <span data-ttu-id="b91e8-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b91e8-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b91e8-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b91e8-124">Namespace</span></span><br/> | <span data-ttu-id="b91e8-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b91e8-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b91e8-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="b91e8-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b91e8-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b91e8-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91e8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b91e8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91e8-129">**IWMPMedia. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b91e8-129">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b91e8-130">**IWMPMedia. getItemInfoByAtom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b91e8-130">**IWMPMedia.getItemInfoByAtom (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b91e8-131">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b91e8-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





