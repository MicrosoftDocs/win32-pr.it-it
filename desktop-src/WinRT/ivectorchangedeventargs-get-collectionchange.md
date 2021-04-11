---
description: Ottiene il tipo di modifica che si è verificata nel vettore.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Metodo IVectorChangedEventArgs:: get_CollectionChange (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226098"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a><span data-ttu-id="c461c-103">Metodo IVectorChangedEventArgs:: Get \_ CollectionChange</span><span class="sxs-lookup"><span data-stu-id="c461c-103">IVectorChangedEventArgs::get\_CollectionChange method</span></span>

<span data-ttu-id="c461c-104">Ottiene il tipo di modifica che si è verificata nel vettore.</span><span class="sxs-lookup"><span data-stu-id="c461c-104">Gets the type of change that occurred in the vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c461c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c461c-105">Syntax</span></span>


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a><span data-ttu-id="c461c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c461c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c461c-107">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c461c-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c461c-108">Tipo: \**CollectionChange \** _</span><span class="sxs-lookup"><span data-stu-id="c461c-108">Type: \**CollectionChange\** _</span></span>

<span data-ttu-id="c461c-109">Valore dell'enumerazione [_ *CollectionChange* \*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) che descrive la modifica.</span><span class="sxs-lookup"><span data-stu-id="c461c-109">A value from the [_ *CollectionChange*\*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) enumeration that describes the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c461c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c461c-110">Return value</span></span>

<span data-ttu-id="c461c-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c461c-111">Type: **HRESULT**</span></span>

<span data-ttu-id="c461c-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c461c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c461c-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c461c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c461c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c461c-114">Requirements</span></span>



| <span data-ttu-id="c461c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c461c-115">Requirement</span></span> | <span data-ttu-id="c461c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c461c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c461c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c461c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c461c-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c461c-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="c461c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c461c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c461c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c461c-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="c461c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c461c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c461c-122"><dt>IVectorChangedEventArgs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c461c-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c461c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c461c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c461c-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="c461c-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 
