---
title: Metodo IWMPLibrary identico
description: Il metodo IsValid restituisce un valore che indica se l'oggetto fornito è uguale a quello corrente.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- Metodo di Media Player di Windows identico
- Metodo identico Media Player Windows, interfaccia IWMPLibrary
- Interfaccia IWMPLibrary Windows Media Player, metodo identico
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332426"
---
# <a name="iwmplibraryisidentical-method"></a><span data-ttu-id="4cb66-106">Metodo IWMPLibrary:: IsValid</span><span class="sxs-lookup"><span data-stu-id="4cb66-106">IWMPLibrary::isIdentical method</span></span>

<span data-ttu-id="4cb66-107">Il **Metodo IsValid** restituisce un valore che indica se l'oggetto fornito è uguale a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="4cb66-107">The **isIdentical** method returns a value that indicates whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb66-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cb66-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="4cb66-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cb66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb66-110">*pIWMPLibrary* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cb66-110">*pIWMPLibrary* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb66-111">Interfaccia **wmplib. IWMPLibrary** che rappresenta l'oggetto da confrontare con quello corrente.</span><span class="sxs-lookup"><span data-stu-id="4cb66-111">A **WMPLib.IWMPLibrary** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb66-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cb66-112">Return value</span></span>

<span data-ttu-id="4cb66-113">**System. Boolean** che rappresenta il risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="4cb66-113">A **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="4cb66-114">Il valore **true** indica che gli oggetti sono uguali.</span><span class="sxs-lookup"><span data-stu-id="4cb66-114">The value **true** indicates that the objects are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb66-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cb66-115">Requirements</span></span>



| <span data-ttu-id="4cb66-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cb66-116">Requirement</span></span> | <span data-ttu-id="4cb66-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4cb66-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb66-118">Versione</span><span class="sxs-lookup"><span data-stu-id="4cb66-118">Version</span></span><br/>   | <span data-ttu-id="4cb66-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="4cb66-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="4cb66-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4cb66-120">Namespace</span></span><br/> | <span data-ttu-id="4cb66-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4cb66-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4cb66-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="4cb66-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4cb66-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4cb66-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb66-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cb66-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb66-125">**Interfaccia IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4cb66-125">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





