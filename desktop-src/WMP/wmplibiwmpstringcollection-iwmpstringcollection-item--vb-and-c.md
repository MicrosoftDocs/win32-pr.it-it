---
title: Metodo elemento IWMPStringCollection
description: Il metodo Item restituisce la stringa in corrispondenza dell'indice specificato.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, interfaccia IWMPStringCollection
- Interfaccia IWMPStringCollection Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327141"
---
# <a name="iwmpstringcollectionitem-method"></a><span data-ttu-id="e0a13-106">Metodo IWMPStringCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="e0a13-106">IWMPStringCollection::Item method</span></span>

<span data-ttu-id="e0a13-107">Il metodo **Item** restituisce la stringa in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="e0a13-107">The **Item** method returns the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a13-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0a13-108">Syntax</span></span>


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="e0a13-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0a13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0a13-110">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0a13-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a13-111">**System. Int32** che rappresenta l'indice.</span><span class="sxs-lookup"><span data-stu-id="e0a13-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0a13-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0a13-112">Return value</span></span>

<span data-ttu-id="e0a13-113">**System. String** che rappresenta la stringa in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="e0a13-113">A **System.String** that is the string at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a13-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0a13-114">Remarks</span></span>

<span data-ttu-id="e0a13-115">L'interfaccia **IWMPStringCollection** viene utilizzata per recuperare il set di valori disponibili per un attributo.</span><span class="sxs-lookup"><span data-stu-id="e0a13-115">The **IWMPStringCollection** interface is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="e0a13-116">È ad esempio possibile usare il metodo **IWMPMediaCollection. getAttributeStringCollection** per recuperare un'interfaccia **IWMPStringCollection** che rappresenta tutti i valori per l'attributo Genre all'interno del tipo di supporto audio.</span><span class="sxs-lookup"><span data-stu-id="e0a13-116">For example, the **IWMPMediaCollection.getAttributeStringCollection** method can be used to retrieve an **IWMPStringCollection** interface representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="e0a13-117">Il metodo **Item** può quindi essere usato per scorrere tutti i valori possibili per l'attributo Genre.</span><span class="sxs-lookup"><span data-stu-id="e0a13-117">The **Item** method can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="e0a13-118">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="e0a13-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e0a13-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e0a13-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0a13-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0a13-120">Requirements</span></span>



| <span data-ttu-id="e0a13-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a13-121">Requirement</span></span> | <span data-ttu-id="e0a13-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e0a13-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a13-123">Versione</span><span class="sxs-lookup"><span data-stu-id="e0a13-123">Version</span></span><br/>   | <span data-ttu-id="e0a13-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e0a13-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e0a13-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0a13-125">Namespace</span></span><br/> | <span data-ttu-id="e0a13-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e0a13-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e0a13-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="e0a13-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e0a13-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e0a13-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a13-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0a13-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a13-130">**IWMPMediaCollection. getAttributeStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a13-130">**IWMPMediaCollection.getAttributeStringCollection (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a13-131">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a13-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a13-132">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a13-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0a13-133">**Interfaccia IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0a13-133">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





