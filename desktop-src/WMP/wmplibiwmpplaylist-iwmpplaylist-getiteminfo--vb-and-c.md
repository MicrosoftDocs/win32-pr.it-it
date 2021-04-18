---
title: Metodo IWMPPlaylist getItemInfo
description: Il metodo getItemInfo restituisce il valore di un attributo della playlist specificato in base al nome.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330976"
---
# <a name="iwmpplaylistgetiteminfo-method"></a><span data-ttu-id="f9b7d-106">Metodo IWMPPlaylist:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="f9b7d-106">IWMPPlaylist::getItemInfo method</span></span>

<span data-ttu-id="f9b7d-107">Il metodo **GetItemInfo** restituisce il valore di un attributo della playlist specificato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="f9b7d-107">The **getItemInfo** method returns the value of a playlist attribute specified by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b7d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9b7d-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="f9b7d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9b7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9b7d-110">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9b7d-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b7d-111">**System. String** che rappresenta il nome dell'attributo playlist.</span><span class="sxs-lookup"><span data-stu-id="f9b7d-111">A **System.String** that is the name of the playlist attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9b7d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9b7d-112">Return value</span></span>

<span data-ttu-id="f9b7d-113">**System. String** che corrisponde al valore dell'attributo playlist.</span><span class="sxs-lookup"><span data-stu-id="f9b7d-113">A **System.String** that is the value of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b7d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9b7d-114">Remarks</span></span>

<span data-ttu-id="f9b7d-115">Prima di usare questo metodo, è necessario avere accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="f9b7d-115">Before using this method, you must have read access to the library.</span></span> <span data-ttu-id="f9b7d-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f9b7d-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f9b7d-117">Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b7d-117">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b7d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9b7d-118">Requirements</span></span>



| <span data-ttu-id="f9b7d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b7d-119">Requirement</span></span> | <span data-ttu-id="f9b7d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f9b7d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b7d-121">Versione</span><span class="sxs-lookup"><span data-stu-id="f9b7d-121">Version</span></span><br/>   | <span data-ttu-id="f9b7d-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f9b7d-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f9b7d-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9b7d-123">Namespace</span></span><br/> | <span data-ttu-id="f9b7d-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f9b7d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f9b7d-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="f9b7d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f9b7d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f9b7d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b7d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9b7d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b7d-128">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9b7d-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9b7d-129">**IWMPPlaylist. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9b7d-129">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





