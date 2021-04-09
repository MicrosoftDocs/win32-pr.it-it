---
title: Messaggio DRV_OPEN (mmsystem. h)
description: Indica al driver di aprire una nuova istanza.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121466"
---
# <a name="drv_open-message"></a><span data-ttu-id="47d1e-104">\_Messaggio aperto DRV</span><span class="sxs-lookup"><span data-stu-id="47d1e-104">DRV\_OPEN message</span></span>

<span data-ttu-id="47d1e-105">Indica al driver di aprire una nuova istanza.</span><span class="sxs-lookup"><span data-stu-id="47d1e-105">Directs the driver to open an new instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="47d1e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="47d1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47d1e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="47d1e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="47d1e-108">Identificatore del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="47d1e-108">Identifier of the installable driver.</span></span>

</dd> <dt>

<span data-ttu-id="47d1e-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="47d1e-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="47d1e-110">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="47d1e-110">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="47d1e-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="47d1e-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="47d1e-112">Indirizzo di una stringa di caratteri wide con terminazione null che specifica le informazioni di configurazione utilizzate per aprire l'istanza.</span><span class="sxs-lookup"><span data-stu-id="47d1e-112">Address of a null-terminated, wide-character string that specifies configuration information used to open the instance.</span></span> <span data-ttu-id="47d1e-113">Se non sono disponibili informazioni di configurazione, la stringa è vuota o il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="47d1e-113">If no configuration information is available, either this string is empty or the parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47d1e-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="47d1e-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="47d1e-115">dati specifici del driver a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="47d1e-115">32-bit driver-specific data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47d1e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47d1e-116">Return Value</span></span>

<span data-ttu-id="47d1e-117">Restituisce un valore diverso da zero se ha esito positivo o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="47d1e-117">Returns a nonzero value if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d1e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="47d1e-118">Remarks</span></span>

<span data-ttu-id="47d1e-119">Se il driver restituisce un valore diverso da zero, il sistema utilizza tale valore come identificatore del driver (il parametro *dwDriverId* ) nei messaggi inviati successivamente all'istanza del driver.</span><span class="sxs-lookup"><span data-stu-id="47d1e-119">If the driver returns a nonzero value, the system uses that value as the driver identifier (the *dwDriverId* parameter) in messages it subsequently sends to the driver instance.</span></span> <span data-ttu-id="47d1e-120">Il driver può restituire qualsiasi tipo di valore come identificatore.</span><span class="sxs-lookup"><span data-stu-id="47d1e-120">The driver can return any type of value as the identifier.</span></span> <span data-ttu-id="47d1e-121">Alcuni driver, ad esempio, restituiscono indirizzi di memoria che puntano a informazioni specifiche dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="47d1e-121">For example, some drivers return memory addresses that point to instance-specific information.</span></span> <span data-ttu-id="47d1e-122">L'utilizzo di questo metodo per specificare gli identificatori per un'istanza di driver consente ai driver di accedere alle informazioni durante l'elaborazione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="47d1e-122">Using this method of specifying identifiers for a driver instance gives the drivers ready access to the information while they are processing messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d1e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47d1e-123">Requirements</span></span>



| <span data-ttu-id="47d1e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d1e-124">Requirement</span></span> | <span data-ttu-id="47d1e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="47d1e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47d1e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47d1e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="47d1e-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="47d1e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="47d1e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47d1e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="47d1e-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="47d1e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="47d1e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47d1e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="47d1e-131"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-131"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d1e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47d1e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d1e-133">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="47d1e-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="47d1e-134">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="47d1e-134">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





