---
title: Messaggio DRV_CONFIGURE (mmsystem. h)
description: Indica al driver installabile di visualizzare la finestra di dialogo di configurazione e consentire all'utente di specificare nuove impostazioni per l'istanza del driver installabile specificata.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- DRV_CONFIGURE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964921"
---
# <a name="drv_configure-message"></a><span data-ttu-id="da1d8-104">\_Messaggio di configurazione DRV</span><span class="sxs-lookup"><span data-stu-id="da1d8-104">DRV\_CONFIGURE message</span></span>

<span data-ttu-id="da1d8-105">Indica al driver installabile di visualizzare la finestra di dialogo di configurazione e consentire all'utente di specificare nuove impostazioni per l'istanza del driver installabile specificata.</span><span class="sxs-lookup"><span data-stu-id="da1d8-105">Directs the installable driver to display its configuration dialog box and let the user specify new settings for the given installable driver instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="da1d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da1d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1d8-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="da1d8-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="da1d8-108">Identificatore del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="da1d8-108">Identifier of the installable driver.</span></span> <span data-ttu-id="da1d8-109">Si tratta dello stesso valore restituito in precedenza dal driver dal messaggio [**\_ aperto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="da1d8-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="da1d8-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="da1d8-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="da1d8-111">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="da1d8-111">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="da1d8-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="da1d8-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="da1d8-113">Handle della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="da1d8-113">Handle of the parent window.</span></span> <span data-ttu-id="da1d8-114">Questa finestra viene utilizzata come finestra padre per la finestra di dialogo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="da1d8-114">This window is used as the parent window for the configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="da1d8-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="da1d8-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="da1d8-116">Indirizzo di una struttura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **null**.</span><span class="sxs-lookup"><span data-stu-id="da1d8-116">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="da1d8-117">Se la struttura è specificata, contiene i nomi della chiave del registro di sistema e il valore associato al driver.</span><span class="sxs-lookup"><span data-stu-id="da1d8-117">If the structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1d8-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da1d8-118">Return Value</span></span>

<span data-ttu-id="da1d8-119">Restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="da1d8-119">Returns one of these values:</span></span>



| <span data-ttu-id="da1d8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1d8-120">Requirement</span></span> | <span data-ttu-id="da1d8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="da1d8-121">Value</span></span> |
|-----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da1d8-122">DRVCNF \_ OK</span><span class="sxs-lookup"><span data-stu-id="da1d8-122">DRVCNF\_OK</span></span>      | <span data-ttu-id="da1d8-123">La configurazione è stata completata. non sono necessarie altre azioni.</span><span class="sxs-lookup"><span data-stu-id="da1d8-123">The configuration is successful; no further action is required.</span></span>                                    |
| <span data-ttu-id="da1d8-124">\_annullamento DRVCNF</span><span class="sxs-lookup"><span data-stu-id="da1d8-124">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="da1d8-125">L'utente ha annullato la finestra di dialogo; non sono necessarie altre azioni.</span><span class="sxs-lookup"><span data-stu-id="da1d8-125">The user canceled the dialog box; no further action is required.</span></span>                                   |
| <span data-ttu-id="da1d8-126">\_riavvio DRVCNF</span><span class="sxs-lookup"><span data-stu-id="da1d8-126">DRVCNF\_RESTART</span></span> | <span data-ttu-id="da1d8-127">La configurazione ha esito positivo, ma le modifiche non diventano effettive fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="da1d8-127">The configuration is successful, but the changes do not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="da1d8-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="da1d8-128">Remarks</span></span>

<span data-ttu-id="da1d8-129">Alcuni driver installabili accodano informazioni di configurazione al valore assegnato al valore del registro di sistema associato al driver.</span><span class="sxs-lookup"><span data-stu-id="da1d8-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

<span data-ttu-id="da1d8-130">I \_ valori restituiti da DRV Cancel, DRV \_ OK e DRV \_ Restart sono obsoleti e sono stati sostituiti rispettivamente da DRVCNF \_ Cancel, DRVCNF \_ OK e DRVCNF \_ restart.</span><span class="sxs-lookup"><span data-stu-id="da1d8-130">The DRV\_CANCEL, DRV\_OK, and DRV\_RESTART return values are obsolete; they have been replaced by DRVCNF\_CANCEL, DRVCNF\_OK, and DRVCNF\_RESTART, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1d8-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da1d8-131">Requirements</span></span>



| <span data-ttu-id="da1d8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1d8-132">Requirement</span></span> | <span data-ttu-id="da1d8-133">Valore</span><span class="sxs-lookup"><span data-stu-id="da1d8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da1d8-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da1d8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="da1d8-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da1d8-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="da1d8-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da1d8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="da1d8-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da1d8-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="da1d8-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da1d8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="da1d8-139"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da1d8-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1d8-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da1d8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1d8-141">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="da1d8-141">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="da1d8-142">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="da1d8-142">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

