---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere comando Invia un blocco di comandi MTP, seguito da una fase di dati. I dati vengono inviati dall'host al dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330579"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a><span data-ttu-id="ed0f7-104">Comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere comando</span><span class="sxs-lookup"><span data-stu-id="ed0f7-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE Command</span></span>

<span data-ttu-id="ed0f7-105">Il comando **WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere** comando Invia un blocco di comandi MTP, seguito da una fase di dati.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command sends an MTP command block, which is followed by a data phase.</span></span> <span data-ttu-id="ed0f7-106">I dati vengono inviati dall'host al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-106">The data is sent from the host to the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="ed0f7-107">Categoria</span><span class="sxs-lookup"><span data-stu-id="ed0f7-107">Command category</span></span>

<span data-ttu-id="ed0f7-108">**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="ed0f7-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="ed0f7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed0f7-109">Parameters</span></span>

<span data-ttu-id="ed0f7-110">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="ed0f7-111">Parametro</span><span class="sxs-lookup"><span data-stu-id="ed0f7-111">Parameter</span></span>                                                | <span data-ttu-id="ed0f7-112">VarType</span><span class="sxs-lookup"><span data-stu-id="ed0f7-112">VarType</span></span> | <span data-ttu-id="ed0f7-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed0f7-113">Description</span></span>                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0f7-114">**\_Proprietà WPD \_ \_ \_ codice operativo MTP \_ ext**</span><span class="sxs-lookup"><span data-stu-id="ed0f7-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>             | <span data-ttu-id="ed0f7-115">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="ed0f7-115">VT\_UI4</span></span> | <span data-ttu-id="ed0f7-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-116">Required.</span></span> <span data-ttu-id="ed0f7-117">Identifica un codice operativo MTP esteso dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                              |
| <span data-ttu-id="ed0f7-118">**\_Proprietà WPD \_ - \_ \_ parametri operazione MTP ext \_**</span><span class="sxs-lookup"><span data-stu-id="ed0f7-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span>           | <span data-ttu-id="ed0f7-119">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="ed0f7-119">VT\_UI4</span></span> | <span data-ttu-id="ed0f7-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-120">Required.</span></span> <span data-ttu-id="ed0f7-121">Raccolta **IPortableDevicePropVariantCollection** che identifica i parametri obbligatori per il codice operativo del fornitore.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-121">An **IPortableDevicePropVariantCollection** collection that identifies the required parameters for the vendor operation code.</span></span> |
| <span data-ttu-id="ed0f7-122">**\_Proprietà WPD \_ MTP \_ \_ trasferimento \_ dati totali- \_ \_ dimensioni dati**</span><span class="sxs-lookup"><span data-stu-id="ed0f7-122">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span> | <span data-ttu-id="ed0f7-123">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="ed0f7-123">VT\_UI8</span></span> | <span data-ttu-id="ed0f7-124">Obbligatorio. specifica le dimensioni totali dei dati, in byte, esclusi gli overhead, da inviare al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-124">Required.Specifies the total data size, in bytes, excluding any overhead, to be sent to device.</span></span>                                         |



 

## <a name="return-value"></a><span data-ttu-id="ed0f7-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed0f7-125">Return Value</span></span>

<span data-ttu-id="ed0f7-126">Il driver restituisce i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-126">The driver returns the following results.</span></span>



| <span data-ttu-id="ed0f7-127">Risultato</span><span class="sxs-lookup"><span data-stu-id="ed0f7-127">Result</span></span>                                                       | <span data-ttu-id="ed0f7-128">VarType</span><span class="sxs-lookup"><span data-stu-id="ed0f7-128">VarType</span></span>    | <span data-ttu-id="ed0f7-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed0f7-129">Description</span></span>                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0f7-130">**\_Proprietà WPD \_ MTP \_ ext \_ Optimal \_ Transfer \_ buffer \_ size**</span><span class="sxs-lookup"><span data-stu-id="ed0f7-130">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="ed0f7-131">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="ed0f7-131">VT\_UI4</span></span>    | <span data-ttu-id="ed0f7-132">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-132">Required.</span></span> <span data-ttu-id="ed0f7-133">Specifica la dimensione ottimale del buffer di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-133">Specifies the optimal size of the transfer buffer.</span></span>                       |
| <span data-ttu-id="ed0f7-134">**Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed0f7-134">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="ed0f7-135">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="ed0f7-135">VT\_LPWSTR</span></span> | <span data-ttu-id="ed0f7-136">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-136">Optional.</span></span> <span data-ttu-id="ed0f7-137">Identificatore di contesto utilizzato dal driver per i trasferimenti di dati successivi.</span><span class="sxs-lookup"><span data-stu-id="ed0f7-137">A context identifier that the driver uses for subsequent data transfers.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="ed0f7-138">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="ed0f7-138">Calling Methods</span></span>

<span data-ttu-id="ed0f7-139">Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="ed0f7-139">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed0f7-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed0f7-140">Requirements</span></span>



| <span data-ttu-id="ed0f7-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed0f7-141">Requirement</span></span> | <span data-ttu-id="ed0f7-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ed0f7-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0f7-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed0f7-143">Header</span></span><br/> | <dl> <span data-ttu-id="ed0f7-144"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed0f7-144"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed0f7-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed0f7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed0f7-146">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="ed0f7-146">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




