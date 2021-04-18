---
title: Metodo IWMPStringCollection2 getItemInfo
description: Il metodo getItemInfo restituisce la stringa corrispondente all'indice e al nome dell'elemento della raccolta di stringhe specificato.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331727"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a><span data-ttu-id="1af37-106">Metodo IWMPStringCollection2:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="1af37-106">IWMPStringCollection2::getItemInfo method</span></span>

<span data-ttu-id="1af37-107">Il metodo **GetItemInfo** restituisce la stringa corrispondente all'indice e al nome dell'elemento della raccolta di stringhe specificato.</span><span class="sxs-lookup"><span data-stu-id="1af37-107">The **getItemInfo** method returns the string corresponding to the specified string collection item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af37-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1af37-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="1af37-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1af37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af37-110">*lCollectionIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1af37-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1af37-111">**System. Int32** che specifica l'indice in base zero dell'elemento della raccolta di stringhe da cui ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="1af37-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="1af37-112">*bstrItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1af37-112">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1af37-113">**System. String** che rappresenta il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="1af37-113">The **System.String** that is the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af37-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1af37-114">Return value</span></span>

<span data-ttu-id="1af37-115">**System. String** che rappresenta il nome dell'elemento della raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="1af37-115">The **System.String** that is the name of the string collection item.</span></span> <span data-ttu-id="1af37-116">Per gli attributi il cui valore sottostante è **System. Boolean**, viene restituita la stringa "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="1af37-116">For attributes whose underlying value is **System.Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="1af37-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1af37-117">Remarks</span></span>

<span data-ttu-id="1af37-118">Per recuperare gli attributi con più valori e attributi con valori complessi, usare il metodo **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="1af37-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="1af37-119">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="1af37-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="1af37-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1af37-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1af37-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1af37-121">Requirements</span></span>



| <span data-ttu-id="1af37-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af37-122">Requirement</span></span> | <span data-ttu-id="1af37-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1af37-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1af37-124">Versione</span><span class="sxs-lookup"><span data-stu-id="1af37-124">Version</span></span><br/>   | <span data-ttu-id="1af37-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="1af37-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="1af37-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1af37-126">Namespace</span></span><br/> | <span data-ttu-id="1af37-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1af37-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1af37-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="1af37-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1af37-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1af37-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af37-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1af37-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af37-131">**Interfaccia IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="1af37-131">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1af37-132">**IWMPStringCollection2. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1af37-132">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





