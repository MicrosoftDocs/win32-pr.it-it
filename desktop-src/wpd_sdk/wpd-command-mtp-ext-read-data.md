---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ Read \_ Data recupera i dati dal dispositivo dopo l'esecuzione del comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ i dati \_ da \_ leggere.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: Comando WPD_COMMAND_MTP_EXT_READ_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330567"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a><span data-ttu-id="691d8-103">Comando WPD \_ comando \_ MTP \_ ext \_ Read \_ Data</span><span class="sxs-lookup"><span data-stu-id="691d8-103">WPD\_COMMAND\_MTP\_EXT\_READ\_DATA Command</span></span>

<span data-ttu-id="691d8-104">Il comando **WPD \_ comando \_ MTP \_ ext \_ Read \_ Data** recupera i dati dal dispositivo dopo l'esecuzione del comando **WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ i dati \_ da \_ leggere** .</span><span class="sxs-lookup"><span data-stu-id="691d8-104">The **WPD\_COMMAND\_MTP\_EXT\_READ\_DATA** command retrieves data from the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="691d8-105">Categoria</span><span class="sxs-lookup"><span data-stu-id="691d8-105">Command category</span></span>

<span data-ttu-id="691d8-106">**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="691d8-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="691d8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="691d8-107">Parameters</span></span>

<span data-ttu-id="691d8-108">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="691d8-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="691d8-109">Parametro</span><span class="sxs-lookup"><span data-stu-id="691d8-109">Parameter</span></span>                                                   | <span data-ttu-id="691d8-110">VarType</span><span class="sxs-lookup"><span data-stu-id="691d8-110">VarType</span></span>             | <span data-ttu-id="691d8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="691d8-111">Description</span></span>                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="691d8-112">**Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="691d8-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>              | <span data-ttu-id="691d8-113">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="691d8-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="691d8-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="691d8-114">Required.</span></span> <span data-ttu-id="691d8-115">Identifica il contesto restituito dalla chiamata precedente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="691d8-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="691d8-116">**\_Proprietà WPD \_ MTP \_ trasferimento ext ext numero \_ \_ \_ \_ di byte da \_ leggere**</span><span class="sxs-lookup"><span data-stu-id="691d8-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_READ**</span></span> | <span data-ttu-id="691d8-117">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="691d8-117">VT\_UI4</span></span>             | <span data-ttu-id="691d8-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="691d8-118">Required.</span></span> <span data-ttu-id="691d8-119">Specifica il numero di byte da leggere.</span><span class="sxs-lookup"><span data-stu-id="691d8-119">Specifies the number of bytes to read.</span></span>                                       |
| <span data-ttu-id="691d8-120">**\_Proprietà WPD \_ MTP \_ \_ Transfer \_ Data**</span><span class="sxs-lookup"><span data-stu-id="691d8-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                 | <span data-ttu-id="691d8-121">VT \_ vettore \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="691d8-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="691d8-122">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="691d8-122">Required.</span></span> <span data-ttu-id="691d8-123">Identifica il buffer in cui vengono copiati i dati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="691d8-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="691d8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="691d8-124">Return Value</span></span>

<span data-ttu-id="691d8-125">Il driver restituisce i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="691d8-125">The driver returns the following results.</span></span>



| <span data-ttu-id="691d8-126">Risultato</span><span class="sxs-lookup"><span data-stu-id="691d8-126">Result</span></span>                                                  | <span data-ttu-id="691d8-127">VarType</span><span class="sxs-lookup"><span data-stu-id="691d8-127">VarType</span></span>             | <span data-ttu-id="691d8-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="691d8-128">Description</span></span>                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| <span data-ttu-id="691d8-129">**\_Proprietà WPD \_ MTP Transfer numero di \_ \_ \_ \_ byte \_ letti**</span><span class="sxs-lookup"><span data-stu-id="691d8-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_READ**</span></span> | <span data-ttu-id="691d8-130">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="691d8-130">VT\_UI4</span></span>             | <span data-ttu-id="691d8-131">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="691d8-131">Required.</span></span> <span data-ttu-id="691d8-132">Specifica il numero di byte ricevuti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="691d8-132">Specifies the number of bytes received from the device.</span></span> |
| <span data-ttu-id="691d8-133">**\_Proprietà WPD \_ MTP \_ \_ Transfer \_ Data**</span><span class="sxs-lookup"><span data-stu-id="691d8-133">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>             | <span data-ttu-id="691d8-134">VT \_ vettore \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="691d8-134">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="691d8-135">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="691d8-135">Required.</span></span> <span data-ttu-id="691d8-136">Buffer che contiene i dati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="691d8-136">The buffer that contains the device data.</span></span>               |



 

## <a name="calling-methods"></a><span data-ttu-id="691d8-137">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="691d8-137">Calling Methods</span></span>

<span data-ttu-id="691d8-138">Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="691d8-138">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="691d8-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="691d8-139">Requirements</span></span>



| <span data-ttu-id="691d8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="691d8-140">Requirement</span></span> | <span data-ttu-id="691d8-141">Valore</span><span class="sxs-lookup"><span data-stu-id="691d8-141">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="691d8-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="691d8-142">Header</span></span><br/> | <dl> <span data-ttu-id="691d8-143"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="691d8-143"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="691d8-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="691d8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="691d8-145">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="691d8-145">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




