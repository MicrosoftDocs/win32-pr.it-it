---
title: Metodo IWMPCdromBurn non disponibile
description: Il metodo disavailable fornisce informazioni sull'unità CD e sui supporti.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- Metodo di Windows Media Player disponibile
- Metodo di Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo disavailable
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329658"
---
# <a name="iwmpcdromburnisavailable-method"></a><span data-ttu-id="aff63-106">Metodo IWMPCdromBurn:: unavailable</span><span class="sxs-lookup"><span data-stu-id="aff63-106">IWMPCdromBurn::isAvailable method</span></span>

<span data-ttu-id="aff63-107">Il metodo **disavailable** fornisce informazioni sull'unità CD e sui supporti.</span><span class="sxs-lookup"><span data-stu-id="aff63-107">The **isAvailable** method provides information about the CD drive and media.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff63-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aff63-108">Syntax</span></span>


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a><span data-ttu-id="aff63-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aff63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff63-110">*bstrItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aff63-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aff63-111">**System. String** che contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="aff63-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="aff63-112">Valore</span><span class="sxs-lookup"><span data-stu-id="aff63-112">Value</span></span> | <span data-ttu-id="aff63-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aff63-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="aff63-114">Bruciare</span><span class="sxs-lookup"><span data-stu-id="aff63-114">Burn</span></span>  | <span data-ttu-id="aff63-115">L'unità è un masterizzatore CD.</span><span class="sxs-lookup"><span data-stu-id="aff63-115">The drive is a CD burner.</span></span>   |
| <span data-ttu-id="aff63-116">Disco</span><span class="sxs-lookup"><span data-stu-id="aff63-116">Disc</span></span>  | <span data-ttu-id="aff63-117">Nell'unità è presente un CD.</span><span class="sxs-lookup"><span data-stu-id="aff63-117">There is a CD in the drive.</span></span> |
| <span data-ttu-id="aff63-118">Cancellazione</span><span class="sxs-lookup"><span data-stu-id="aff63-118">Erase</span></span> | <span data-ttu-id="aff63-119">È possibile cancellare il CD.</span><span class="sxs-lookup"><span data-stu-id="aff63-119">The CD can be erased.</span></span>       |
| <span data-ttu-id="aff63-120">Scrittura</span><span class="sxs-lookup"><span data-stu-id="aff63-120">Write</span></span> | <span data-ttu-id="aff63-121">È possibile scrivere in un CD.</span><span class="sxs-lookup"><span data-stu-id="aff63-121">The CD can be written to.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff63-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aff63-122">Return value</span></span>

<span data-ttu-id="aff63-123">**System. Boolean** che indica il risultato.</span><span class="sxs-lookup"><span data-stu-id="aff63-123">A **System.Boolean** that indicates the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff63-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aff63-124">Requirements</span></span>



| <span data-ttu-id="aff63-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff63-125">Requirement</span></span> | <span data-ttu-id="aff63-126">Valore</span><span class="sxs-lookup"><span data-stu-id="aff63-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff63-127">Versione</span><span class="sxs-lookup"><span data-stu-id="aff63-127">Version</span></span><br/>   | <span data-ttu-id="aff63-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="aff63-128">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="aff63-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aff63-129">Namespace</span></span><br/> | <span data-ttu-id="aff63-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="aff63-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="aff63-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="aff63-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="aff63-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="aff63-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff63-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aff63-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff63-134">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="aff63-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





