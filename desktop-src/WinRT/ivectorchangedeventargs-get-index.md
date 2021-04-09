---
description: Ottiene la posizione nel vettore in cui si è verificata la modifica.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Metodo IVectorChangedEventArgs:: get_Index (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049492"
---
# <a name="ivectorchangedeventargsget_index-method"></a><span data-ttu-id="b252a-103">Metodo IVectorChangedEventArgs:: Get \_ index</span><span class="sxs-lookup"><span data-stu-id="b252a-103">IVectorChangedEventArgs::get\_Index method</span></span>

<span data-ttu-id="b252a-104">Ottiene la posizione nel vettore in cui si è verificata la modifica.</span><span class="sxs-lookup"><span data-stu-id="b252a-104">Gets the position in the vector where the change occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="b252a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b252a-105">Syntax</span></span>


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a><span data-ttu-id="b252a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b252a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b252a-107">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b252a-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b252a-108">Tipo: \**unsigned \** _</span><span class="sxs-lookup"><span data-stu-id="b252a-108">Type: \**unsigned\** _</span></span>

<span data-ttu-id="b252a-109">Posizione in base zero nel vettore in cui si è verificata la modifica, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="b252a-109">The zero-based position in the vector where the change occurred, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b252a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b252a-110">Return value</span></span>

<span data-ttu-id="b252a-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b252a-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b252a-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b252a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b252a-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b252a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b252a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b252a-114">Requirements</span></span>



| <span data-ttu-id="b252a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b252a-115">Requirement</span></span> | <span data-ttu-id="b252a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b252a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b252a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b252a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b252a-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b252a-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="b252a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b252a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b252a-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b252a-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="b252a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b252a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b252a-122"><dt>IVectorChangedEventArgs. h</dt></span><span class="sxs-lookup"><span data-stu-id="b252a-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b252a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b252a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b252a-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="b252a-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 




