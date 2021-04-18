---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ Write \_ Data invia dati al dispositivo dopo l'esecuzione del comando WPD \_ Command \_ MTP \_ ext \_ Execute \_ \_ con \_ i dati \_ da \_ scrivere.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: Comando WPD_COMMAND_MTP_EXT_WRITE_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330565"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a><span data-ttu-id="43b17-103">Comando WPD \_ comando \_ MTP \_ ext \_ Write \_ Data</span><span class="sxs-lookup"><span data-stu-id="43b17-103">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA Command</span></span>

<span data-ttu-id="43b17-104">Il comando **WPD \_ comando \_ MTP \_ ext \_ Write \_ Data** invia dati al dispositivo dopo l'esecuzione del comando **WPD \_ Command \_ MTP \_ ext \_ Execute \_ \_ con \_ i dati \_ da \_ scrivere** .</span><span class="sxs-lookup"><span data-stu-id="43b17-104">The **WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA** command sends data to the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="43b17-105">Categoria</span><span class="sxs-lookup"><span data-stu-id="43b17-105">Command category</span></span>

<span data-ttu-id="43b17-106">**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="43b17-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="43b17-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="43b17-107">Parameters</span></span>

<span data-ttu-id="43b17-108">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="43b17-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="43b17-109">Parametro</span><span class="sxs-lookup"><span data-stu-id="43b17-109">Parameter</span></span>                                                    | <span data-ttu-id="43b17-110">VarType</span><span class="sxs-lookup"><span data-stu-id="43b17-110">VarType</span></span>             | <span data-ttu-id="43b17-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43b17-111">Description</span></span>                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43b17-112">**Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="43b17-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="43b17-113">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="43b17-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="43b17-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="43b17-114">Required.</span></span> <span data-ttu-id="43b17-115">Identifica il contesto restituito dalla chiamata precedente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43b17-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="43b17-116">**\_Proprietà WPD \_ MTP \_ trasferimento EXT numero \_ \_ \_ \_ di byte da \_ scrivere**</span><span class="sxs-lookup"><span data-stu-id="43b17-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_WRITE**</span></span> | <span data-ttu-id="43b17-117">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="43b17-117">VT\_UI4</span></span>             | <span data-ttu-id="43b17-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="43b17-118">Required.</span></span> <span data-ttu-id="43b17-119">Specifica il numero di byte da scrivere.</span><span class="sxs-lookup"><span data-stu-id="43b17-119">Specifies the number of bytes to write.</span></span>                                      |
| <span data-ttu-id="43b17-120">**\_Proprietà WPD \_ MTP \_ \_ Transfer \_ Data**</span><span class="sxs-lookup"><span data-stu-id="43b17-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                  | <span data-ttu-id="43b17-121">VT \_ vettore \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="43b17-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="43b17-122">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="43b17-122">Required.</span></span> <span data-ttu-id="43b17-123">Identifica il buffer in cui vengono copiati i dati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43b17-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="43b17-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43b17-124">Return Value</span></span>

<span data-ttu-id="43b17-125">Il driver restituisce i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="43b17-125">The driver returns the following results.</span></span>



| <span data-ttu-id="43b17-126">Risultato</span><span class="sxs-lookup"><span data-stu-id="43b17-126">Result</span></span>                                                     | <span data-ttu-id="43b17-127">VarType</span><span class="sxs-lookup"><span data-stu-id="43b17-127">VarType</span></span> | <span data-ttu-id="43b17-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43b17-128">Description</span></span>                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| <span data-ttu-id="43b17-129">**\_Proprietà WPD \_ MTP \_ Transfer EXT numero \_ \_ \_ byte \_ scritti**</span><span class="sxs-lookup"><span data-stu-id="43b17-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_WRITTEN**</span></span> | <span data-ttu-id="43b17-130">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="43b17-130">VT\_UI4</span></span> | <span data-ttu-id="43b17-131">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="43b17-131">Required.</span></span> <span data-ttu-id="43b17-132">Specifica il numero di byte inviati al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43b17-132">Specifies the number of bytes sent to the device..</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="43b17-133">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="43b17-133">Calling Methods</span></span>

<span data-ttu-id="43b17-134">Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="43b17-134">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="43b17-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43b17-135">Requirements</span></span>



| <span data-ttu-id="43b17-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="43b17-136">Requirement</span></span> | <span data-ttu-id="43b17-137">Valore</span><span class="sxs-lookup"><span data-stu-id="43b17-137">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b17-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43b17-138">Header</span></span><br/> | <dl> <span data-ttu-id="43b17-139"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="43b17-139"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b17-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43b17-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b17-141">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="43b17-141">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




