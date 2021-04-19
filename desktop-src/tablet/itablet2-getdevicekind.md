---
description: Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto Tablet, ad esempio il mouse, la penna o il tocco.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'Metodo ITablet2:: GetDeviceKind'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313920"
---
# <a name="itablet2getdevicekind-method"></a><span data-ttu-id="ee1aa-103">Metodo ITablet2:: GetDeviceKind</span><span class="sxs-lookup"><span data-stu-id="ee1aa-103">ITablet2::GetDeviceKind method</span></span>

<span data-ttu-id="ee1aa-104">Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto Tablet, ad esempio il mouse, la penna o il tocco.</span><span class="sxs-lookup"><span data-stu-id="ee1aa-104">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee1aa-105">Syntax</span></span>


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a><span data-ttu-id="ee1aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee1aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1aa-107">*pKind* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ee1aa-107">*pKind* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1aa-108">Valore di enumerazione che indica il tipo di Tablet, ad esempio il mouse, la penna o il tocco.</span><span class="sxs-lookup"><span data-stu-id="ee1aa-108">Enumeration value that indicates the type of tablet such as mouse, pen or touch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1aa-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee1aa-109">Return value</span></span>

<span data-ttu-id="ee1aa-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ee1aa-110">This method can return one of these values.</span></span>



| <span data-ttu-id="ee1aa-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ee1aa-111">Return code</span></span>                                                                            | <span data-ttu-id="ee1aa-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1aa-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ee1aa-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee1aa-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ee1aa-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ee1aa-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="ee1aa-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="ee1aa-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ee1aa-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ee1aa-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee1aa-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee1aa-117">Remarks</span></span>

<span data-ttu-id="ee1aa-118">Questa interfaccia e questo metodo sono stati introdotti in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee1aa-118">This interface and method were introduced in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee1aa-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee1aa-119">Requirements</span></span>



| <span data-ttu-id="ee1aa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee1aa-120">Requirement</span></span> | <span data-ttu-id="ee1aa-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1aa-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1aa-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee1aa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ee1aa-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ee1aa-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ee1aa-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee1aa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ee1aa-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ee1aa-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ee1aa-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="ee1aa-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee1aa-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee1aa-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee1aa-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee1aa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1aa-129">**Interfaccia ITablet2**</span><span class="sxs-lookup"><span data-stu-id="ee1aa-129">**ITablet2 Interface**</span></span>](itablet2.md)
</dt> <dt>

[<span data-ttu-id="ee1aa-130">**Enumerazione del tipo di \_ dispositivo Tablet \_**</span><span class="sxs-lookup"><span data-stu-id="ee1aa-130">**TABLET\_DEVICE\_KIND Enumeration**</span></span>](tablet-device-kind.md)
</dt> <dt>

[<span data-ttu-id="ee1aa-131">**Interfaccia ITablet**</span><span class="sxs-lookup"><span data-stu-id="ee1aa-131">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




