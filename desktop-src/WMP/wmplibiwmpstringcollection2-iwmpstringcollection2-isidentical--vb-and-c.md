---
title: Metodo IWMPStringCollection2 identico
description: Il metodo IsValid restituisce un valore che indica se l'oggetto rappresentato dall'interfaccia fornita è identico a quello corrente.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- Metodo di Media Player di Windows identico
- Metodo identico Media Player Windows, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player, metodo identico
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331725"
---
# <a name="iwmpstringcollection2isidentical-method"></a><span data-ttu-id="88385-106">Metodo IWMPStringCollection2:: IsValid</span><span class="sxs-lookup"><span data-stu-id="88385-106">IWMPStringCollection2::isIdentical method</span></span>

<span data-ttu-id="88385-107">Il **Metodo IsValid** restituisce un valore che indica se l'oggetto rappresentato dall'interfaccia fornita è identico a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="88385-107">The **isIdentical** method returns a value indicating whether the object represented by the supplied interface is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="88385-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88385-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="88385-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="88385-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88385-110">*pIWMPStringCollection2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88385-110">*pIWMPStringCollection2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88385-111">Interfaccia **wmplib. IWMPStringCollection2** che rappresenta l'oggetto da confrontare con quello corrente.</span><span class="sxs-lookup"><span data-stu-id="88385-111">The **WMPLib.IWMPStringCollection2** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88385-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88385-112">Return value</span></span>

<span data-ttu-id="88385-113">**System. Boolean** che rappresenta il risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="88385-113">The **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="88385-114">Il valore **true** indica che gli oggetti della raccolta di stringhe sono uguali.</span><span class="sxs-lookup"><span data-stu-id="88385-114">A value of **true** indicates that the string collection objects are the same.</span></span>

## <a name="remarks"></a><span data-ttu-id="88385-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="88385-115">Remarks</span></span>

<span data-ttu-id="88385-116">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="88385-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="88385-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="88385-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88385-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88385-118">Requirements</span></span>



| <span data-ttu-id="88385-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="88385-119">Requirement</span></span> | <span data-ttu-id="88385-120">Valore</span><span class="sxs-lookup"><span data-stu-id="88385-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88385-121">Versione</span><span class="sxs-lookup"><span data-stu-id="88385-121">Version</span></span><br/>   | <span data-ttu-id="88385-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="88385-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="88385-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88385-123">Namespace</span></span><br/> | <span data-ttu-id="88385-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="88385-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="88385-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="88385-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="88385-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="88385-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88385-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88385-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88385-128">**Interfaccia IWMPStringCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="88385-128">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





