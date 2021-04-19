---
title: IWMPPlaylist. AttributeName (VB e C)
description: La proprietà AttributeName (il \_ metodo Get AttributeName in C \) ottiene il nome di un attributo della playlist specificato da un indice.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. AttributeName (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324224"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a><span data-ttu-id="3fd81-104">IWMPPlaylist. AttributeName (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="3fd81-104">IWMPPlaylist.attributeName (VB and C#)</span></span>

<span data-ttu-id="3fd81-105">La proprietà **attributeName** (il metodo **get \_ attributeName** in C#) ottiene il nome di un attributo della playlist specificato da un indice.</span><span class="sxs-lookup"><span data-stu-id="3fd81-105">The **attributeName** property (the **get\_attributeName** method in C#) gets the name of a playlist attribute specified by an index.</span></span>


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a><span data-ttu-id="3fd81-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fd81-106">Parameters</span></span>

<span data-ttu-id="3fd81-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="3fd81-107">*lIndex*</span></span>

<span data-ttu-id="3fd81-108">**System. Int32** che rappresenta l'indice dell'attributo playlist.</span><span class="sxs-lookup"><span data-stu-id="3fd81-108">A **System.Int32** that is the index of the playlist attribute.</span></span>

## <a name="return-value"></a><span data-ttu-id="3fd81-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fd81-109">Return Value</span></span>

<span data-ttu-id="3fd81-110">**System. String** che rappresenta il nome dell'attributo playlist.</span><span class="sxs-lookup"><span data-stu-id="3fd81-110">A **System.String** that is the name of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd81-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fd81-111">Remarks</span></span>

<span data-ttu-id="3fd81-112">**IWMPPlaylist. AttributeName** è una proprietà di sola lettura in Visual Basic che accetta un parametro, mentre in C# viene chiamato il metodo **IWMPPlaylist. Get \_ attributeName** .</span><span class="sxs-lookup"><span data-stu-id="3fd81-112">**IWMPPlaylist.attributeName** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_attributeName** method.</span></span>

<span data-ttu-id="3fd81-113">Il numero di attributi associati a una playlist viene restituito dalla proprietà **IWMPPlaylist. attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="3fd81-113">The number of attributes associated with a playlist is returned by the **IWMPPlaylist.attributeCount** property.</span></span>

<span data-ttu-id="3fd81-114">Il nome restituito da questa proprietà può essere fornito ai metodi **setItemInfo** o **GetItemInfo** per specificare o recuperare un valore per l'attributo denominato.</span><span class="sxs-lookup"><span data-stu-id="3fd81-114">The name returned by this property can be supplied to the **setItemInfo** or **getItemInfo** methods to specify or retrieve a value for the named attribute.</span></span>

<span data-ttu-id="3fd81-115">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3fd81-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="3fd81-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3fd81-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3fd81-117">Per ulteriori informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3fd81-117">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3fd81-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="3fd81-118">Examples</span></span>

<span data-ttu-id="3fd81-119">Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd81-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd81-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fd81-120">Requirements</span></span>



| <span data-ttu-id="3fd81-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd81-121">Requirement</span></span> | <span data-ttu-id="3fd81-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd81-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd81-123">Versione</span><span class="sxs-lookup"><span data-stu-id="3fd81-123">Version</span></span><br/>   | <span data-ttu-id="3fd81-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3fd81-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3fd81-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3fd81-125">Namespace</span></span><br/> | <span data-ttu-id="3fd81-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3fd81-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3fd81-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="3fd81-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3fd81-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3fd81-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd81-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fd81-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd81-130">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3fd81-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3fd81-131">**IWMPPlaylist. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3fd81-131">**IWMPPlaylist.attributeCount (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3fd81-132">**IWMPPlaylist. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3fd81-132">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3fd81-133">**IWMPPlaylist. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3fd81-133">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





