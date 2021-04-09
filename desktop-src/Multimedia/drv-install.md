---
title: Messaggio DRV_INSTALL (mmsystem. h)
description: Notifica al driver che è in fase di installazione. Il driver deve creare e inizializzare le chiavi e i valori del registro di sistema necessari e verificare che i driver e l'hardware di supporto siano installati e configurati correttamente.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- DRV_INSTALL messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964918"
---
# <a name="drv_install-message"></a><span data-ttu-id="13d37-105">\_Messaggio di installazione DRV</span><span class="sxs-lookup"><span data-stu-id="13d37-105">DRV\_INSTALL message</span></span>

<span data-ttu-id="13d37-106">Notifica al driver che è in fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="13d37-106">Notifies the driver that is it being installed.</span></span> <span data-ttu-id="13d37-107">Il driver deve creare e inizializzare le chiavi e i valori del registro di sistema necessari e verificare che i driver e l'hardware di supporto siano installati e configurati correttamente.</span><span class="sxs-lookup"><span data-stu-id="13d37-107">The driver should create and initialize any needed registry keys and values and verify that the supporting drivers and hardware are installed and properly configured.</span></span>

## <a name="parameters"></a><span data-ttu-id="13d37-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="13d37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13d37-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="13d37-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="13d37-110">Identificatore del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="13d37-110">Identifier of the installable driver.</span></span> <span data-ttu-id="13d37-111">Si tratta dello stesso valore restituito in precedenza dal driver dal messaggio [**\_ aperto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="13d37-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="13d37-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="13d37-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="13d37-113">Handle dell'istanza del driver installabile.</span><span class="sxs-lookup"><span data-stu-id="13d37-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="13d37-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="13d37-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="13d37-115">Indirizzo di una struttura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **null**.</span><span class="sxs-lookup"><span data-stu-id="13d37-115">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="13d37-116">Se viene fornita una struttura, contiene i nomi della chiave del registro di sistema e il valore associato al driver.</span><span class="sxs-lookup"><span data-stu-id="13d37-116">If a structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13d37-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13d37-117">Return Value</span></span>

<span data-ttu-id="13d37-118">Restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="13d37-118">Returns one of these values:</span></span>



| <span data-ttu-id="13d37-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d37-119">Requirement</span></span> | <span data-ttu-id="13d37-120">Valore</span><span class="sxs-lookup"><span data-stu-id="13d37-120">Value</span></span> |
|-----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d37-121">DRVCNF \_ OK</span><span class="sxs-lookup"><span data-stu-id="13d37-121">DRVCNF\_OK</span></span>      | <span data-ttu-id="13d37-122">L'installazione è riuscita. non sono necessarie altre azioni.</span><span class="sxs-lookup"><span data-stu-id="13d37-122">The installation is successful; no further action is required.</span></span>                             |
| <span data-ttu-id="13d37-123">\_annullamento DRVCNF</span><span class="sxs-lookup"><span data-stu-id="13d37-123">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="13d37-124">Installazione non riuscita..</span><span class="sxs-lookup"><span data-stu-id="13d37-124">The installation failed..</span></span>                                                                  |
| <span data-ttu-id="13d37-125">\_riavvio DRVCNF</span><span class="sxs-lookup"><span data-stu-id="13d37-125">DRVCNF\_RESTART</span></span> | <span data-ttu-id="13d37-126">L'installazione ha esito positivo, ma non diventa effettiva fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="13d37-126">The installation is successful, but it does not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="13d37-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="13d37-127">Remarks</span></span>

<span data-ttu-id="13d37-128">Il parametro *lParam1* non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="13d37-128">The *lParam1* parameter is not used.</span></span>

<span data-ttu-id="13d37-129">Alcuni driver installabili accodano informazioni di configurazione al valore assegnato al valore del registro di sistema associato al driver.</span><span class="sxs-lookup"><span data-stu-id="13d37-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d37-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13d37-130">Requirements</span></span>



| <span data-ttu-id="13d37-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d37-131">Requirement</span></span> | <span data-ttu-id="13d37-132">Valore</span><span class="sxs-lookup"><span data-stu-id="13d37-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d37-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13d37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="13d37-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13d37-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13d37-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13d37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="13d37-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13d37-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13d37-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13d37-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="13d37-138"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13d37-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d37-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13d37-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d37-140">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="13d37-140">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="13d37-141">Messaggi di driver installabili</span><span class="sxs-lookup"><span data-stu-id="13d37-141">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

