---
description: Il comando \_ WPD \_ MTP \_ ext \_ Execute \_ Command \_ without \_ data \_ Phase Invia un blocco di comandi MTP. A questo comando non è associata alcuna fase di dati successiva.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330576"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a><span data-ttu-id="bf6d7-104">Comando \_ WPD \_ MTP \_ ext \_ Execute \_ Command \_ without \_ data \_ fase Command</span><span class="sxs-lookup"><span data-stu-id="bf6d7-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE Command</span></span>

<span data-ttu-id="bf6d7-105">Il **comando \_ WPD \_ MTP \_ ext \_ Execute \_ Command \_ without \_ data \_ Phase** Invia un blocco di comandi MTP.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE** command sends an MTP command block.</span></span> <span data-ttu-id="bf6d7-106">A questo comando non è associata alcuna fase di dati successiva.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="bf6d7-107">Categoria</span><span class="sxs-lookup"><span data-stu-id="bf6d7-107">Command category</span></span>

<span data-ttu-id="bf6d7-108">**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="bf6d7-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="bf6d7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf6d7-109">Parameters</span></span>

<span data-ttu-id="bf6d7-110">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="bf6d7-111">Parametro</span><span class="sxs-lookup"><span data-stu-id="bf6d7-111">Parameter</span></span>                                      | <span data-ttu-id="bf6d7-112">VarType</span><span class="sxs-lookup"><span data-stu-id="bf6d7-112">VarType</span></span> | <span data-ttu-id="bf6d7-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf6d7-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6d7-114">**\_Proprietà WPD \_ \_ \_ codice operativo MTP \_ ext**</span><span class="sxs-lookup"><span data-stu-id="bf6d7-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="bf6d7-115">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="bf6d7-115">VT\_UI4</span></span> | <span data-ttu-id="bf6d7-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-116">Required.</span></span> <span data-ttu-id="bf6d7-117">Identifica un codice operativo MTP esteso dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="bf6d7-118">**\_Proprietà WPD \_ - \_ \_ parametri operazione MTP ext \_**</span><span class="sxs-lookup"><span data-stu-id="bf6d7-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="bf6d7-119">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="bf6d7-119">VT\_UI4</span></span> | <span data-ttu-id="bf6d7-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-120">Required.</span></span> <span data-ttu-id="bf6d7-121">Oggetto **IPortableDevicePropVariantCollection**, che identifica i parametri obbligatori per il codice operativo del fornitore.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="bf6d7-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf6d7-122">Return Value</span></span>

<span data-ttu-id="bf6d7-123">Il driver restituisce i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-123">The driver returns the following results.</span></span>



| <span data-ttu-id="bf6d7-124">Risultato</span><span class="sxs-lookup"><span data-stu-id="bf6d7-124">Result</span></span>                                        | <span data-ttu-id="bf6d7-125">VarType</span><span class="sxs-lookup"><span data-stu-id="bf6d7-125">VarType</span></span> | <span data-ttu-id="bf6d7-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf6d7-126">Description</span></span>                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6d7-127">**\_Proprietà WPD \_ \_ codice di \_ risposta MTP ext \_**</span><span class="sxs-lookup"><span data-stu-id="bf6d7-127">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="bf6d7-128">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="bf6d7-128">VT\_UI4</span></span> | <span data-ttu-id="bf6d7-129">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-129">Required.</span></span> <span data-ttu-id="bf6d7-130">Codice di risposta al codice operativo del fornitore.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-130">The response code to the vendor operation code.</span></span>                                                                      |
| <span data-ttu-id="bf6d7-131">**\_Proprietà WPD \_ \_ parametri di \_ risposta MTP ext \_**</span><span class="sxs-lookup"><span data-stu-id="bf6d7-131">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="bf6d7-132">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="bf6d7-132">VT\_UI4</span></span> | <span data-ttu-id="bf6d7-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-133">Optional.</span></span> <span data-ttu-id="bf6d7-134">Oggetto **IPortableDevicePropVariantCollection** che identifica i parametri della risposta.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-134">An **IPortableDevicePropVariantCollection** that identifies any response parameters.</span></span> <span data-ttu-id="bf6d7-135">Questa raccolta potrebbe essere vuota.</span><span class="sxs-lookup"><span data-stu-id="bf6d7-135">This collection might be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="bf6d7-136">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="bf6d7-136">Calling Methods</span></span>

<span data-ttu-id="bf6d7-137">Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="bf6d7-137">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf6d7-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf6d7-138">Requirements</span></span>



| <span data-ttu-id="bf6d7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf6d7-139">Requirement</span></span> | <span data-ttu-id="bf6d7-140">Valore</span><span class="sxs-lookup"><span data-stu-id="bf6d7-140">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6d7-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf6d7-141">Header</span></span><br/> | <dl> <span data-ttu-id="bf6d7-142"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf6d7-142"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf6d7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf6d7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf6d7-144">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="bf6d7-144">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




