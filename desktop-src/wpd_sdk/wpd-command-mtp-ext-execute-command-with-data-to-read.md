---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere comando Invia un blocco di comandi MTP, che verrà seguito da una fase di dati. I dati vengono inviati dal dispositivo all'host.
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330580"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a><span data-ttu-id="a0e94-104">Comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere comando</span><span class="sxs-lookup"><span data-stu-id="a0e94-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ Command</span></span>

<span data-ttu-id="a0e94-105">Il comando **WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere** comando Invia un blocco di comandi MTP, che verrà seguito da una fase di dati.</span><span class="sxs-lookup"><span data-stu-id="a0e94-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command sends an MTP command block, which will be followed by a data phase.</span></span> <span data-ttu-id="a0e94-106">I dati vengono inviati dal dispositivo all'host.</span><span class="sxs-lookup"><span data-stu-id="a0e94-106">(The data is sent from the device to the host.)</span></span>

## <a name="command-category"></a><span data-ttu-id="a0e94-107">Categoria</span><span class="sxs-lookup"><span data-stu-id="a0e94-107">Command category</span></span>

<span data-ttu-id="a0e94-108">**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="a0e94-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="a0e94-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0e94-109">Parameters</span></span>

<span data-ttu-id="a0e94-110">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0e94-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="a0e94-111">Parametro</span><span class="sxs-lookup"><span data-stu-id="a0e94-111">Parameter</span></span>                                      | <span data-ttu-id="a0e94-112">VarType</span><span class="sxs-lookup"><span data-stu-id="a0e94-112">VarType</span></span> | <span data-ttu-id="a0e94-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0e94-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e94-114">**\_Proprietà WPD \_ \_ \_ codice operativo MTP \_ ext**</span><span class="sxs-lookup"><span data-stu-id="a0e94-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="a0e94-115">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="a0e94-115">VT\_UI4</span></span> | <span data-ttu-id="a0e94-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0e94-116">Required.</span></span> <span data-ttu-id="a0e94-117">Identifica un codice operativo MTP esteso dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="a0e94-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="a0e94-118">**\_Proprietà WPD \_ - \_ \_ parametri operazione MTP ext \_**</span><span class="sxs-lookup"><span data-stu-id="a0e94-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="a0e94-119">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="a0e94-119">VT\_UI4</span></span> | <span data-ttu-id="a0e94-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0e94-120">Required.</span></span> <span data-ttu-id="a0e94-121">Oggetto **IPortableDevicePropVariantCollection**, che identifica i parametri obbligatori per il codice operativo del fornitore.</span><span class="sxs-lookup"><span data-stu-id="a0e94-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="a0e94-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0e94-122">Return Value</span></span>

<span data-ttu-id="a0e94-123">Il driver restituisce i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0e94-123">The driver returns the following results.</span></span>



| <span data-ttu-id="a0e94-124">Risultato</span><span class="sxs-lookup"><span data-stu-id="a0e94-124">Result</span></span>                                                       | <span data-ttu-id="a0e94-125">VarType</span><span class="sxs-lookup"><span data-stu-id="a0e94-125">VarType</span></span>    | <span data-ttu-id="a0e94-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0e94-126">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e94-127">**\_Proprietà WPD \_ MTP \_ \_ trasferimento \_ dati totali- \_ \_ dimensioni dati**</span><span class="sxs-lookup"><span data-stu-id="a0e94-127">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span>     | <span data-ttu-id="a0e94-128">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="a0e94-128">VT\_UI8</span></span>    | <span data-ttu-id="a0e94-129">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0e94-129">Required.</span></span> <span data-ttu-id="a0e94-130">Restituisce la dimensione totale dei dati, in byte, esclusi gli overhead provenienti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0e94-130">Returns the total data size, in bytes, excluding any overhead coming from the device.</span></span> <span data-ttu-id="a0e94-131">Se il dispositivo segnala un valore sconosciuto DataSize (0xFFFFFFFF), il driver chiamerà ripetutamente **ReadData** fino a quando non viene ricevuto un breve blocco</span><span class="sxs-lookup"><span data-stu-id="a0e94-131">If the device reports unknown datasize (0xFFFFFFFF), the driver should call **ReadData** repeatedly until a short chunk is received</span></span> |
| <span data-ttu-id="a0e94-132">**\_Proprietà WPD \_ MTP \_ ext \_ Optimal \_ Transfer \_ buffer \_ size**</span><span class="sxs-lookup"><span data-stu-id="a0e94-132">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="a0e94-133">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="a0e94-133">VT\_UI4</span></span>    | <span data-ttu-id="a0e94-134">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0e94-134">Optional.</span></span> <span data-ttu-id="a0e94-135">Restituisce la dimensione ottimale del buffer di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="a0e94-135">Returns the optimal size of the transfer buffer.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="a0e94-136">**Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0e94-136">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="a0e94-137">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="a0e94-137">VT\_LPWSTR</span></span> | <span data-ttu-id="a0e94-138">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0e94-138">Required.</span></span> <span data-ttu-id="a0e94-139">Specifica l'identificatore di contesto per i trasferimenti di dati successivi.</span><span class="sxs-lookup"><span data-stu-id="a0e94-139">Specifies the context identifier for subsequent data transfers.</span></span>                                                                                                                                                           |



 

## <a name="calling-methods"></a><span data-ttu-id="a0e94-140">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="a0e94-140">Calling Methods</span></span>

<span data-ttu-id="a0e94-141">Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="a0e94-141">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e94-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0e94-142">Requirements</span></span>



| <span data-ttu-id="a0e94-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0e94-143">Requirement</span></span> | <span data-ttu-id="a0e94-144">Valore</span><span class="sxs-lookup"><span data-stu-id="a0e94-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e94-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0e94-145">Header</span></span><br/> | <dl> <span data-ttu-id="a0e94-146"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0e94-146"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0e94-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0e94-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e94-148">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="a0e94-148">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




