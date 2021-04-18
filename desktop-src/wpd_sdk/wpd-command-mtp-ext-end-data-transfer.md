---
description: Il \_ comando WPD comando \_ MTP \_ ext \_ End \_ data \_ Transfer completa un trasferimento dati e una risposta di lettura dal dispositivo.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: Comando WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331685"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a><span data-ttu-id="8e77a-103">\_Comando WPD comando \_ MTP \_ ext \_ End \_ data \_ Transfer</span><span class="sxs-lookup"><span data-stu-id="8e77a-103">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER Command</span></span>

<span data-ttu-id="8e77a-104">Il comando **WPD \_ comando \_ MTP \_ ext \_ End \_ data \_ Transfer** completa un trasferimento dati e una risposta di lettura dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e77a-104">The **WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER** command completes a data transfer and read response from the device.</span></span> <span data-ttu-id="8e77a-105">Il trasferimento viene avviato tramite il comando [**WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) oppure il comando [**WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) comando.</span><span class="sxs-lookup"><span data-stu-id="8e77a-105">The transfer is initiated by either the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) command or the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) command.</span></span>

## <a name="command-category"></a><span data-ttu-id="8e77a-106">Categoria</span><span class="sxs-lookup"><span data-stu-id="8e77a-106">Command category</span></span>

<span data-ttu-id="8e77a-107">**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="8e77a-107">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="8e77a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e77a-108">Parameters</span></span>

<span data-ttu-id="8e77a-109">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e77a-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="8e77a-110">Parametro</span><span class="sxs-lookup"><span data-stu-id="8e77a-110">Parameter</span></span>                                      | <span data-ttu-id="8e77a-111">VarType</span><span class="sxs-lookup"><span data-stu-id="8e77a-111">VarType</span></span>    | <span data-ttu-id="8e77a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e77a-112">Description</span></span>                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8e77a-113">**Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e77a-113">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span> | <span data-ttu-id="8e77a-114">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="8e77a-114">VT\_LPWSTR</span></span> | <span data-ttu-id="8e77a-115">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8e77a-115">Required.</span></span> <span data-ttu-id="8e77a-116">Identifica il contesto restituito da una chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="8e77a-116">Identifies the context that is returned by an earlier method call.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="8e77a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e77a-117">Return Value</span></span>

<span data-ttu-id="8e77a-118">Il driver restituisce i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e77a-118">The driver returns the following results.</span></span>



| <span data-ttu-id="8e77a-119">Risultato</span><span class="sxs-lookup"><span data-stu-id="8e77a-119">Result</span></span>                                        | <span data-ttu-id="8e77a-120">VarType</span><span class="sxs-lookup"><span data-stu-id="8e77a-120">VarType</span></span> | <span data-ttu-id="8e77a-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e77a-121">Description</span></span>                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e77a-122">**\_Proprietà WPD \_ \_ codice di \_ risposta MTP ext \_**</span><span class="sxs-lookup"><span data-stu-id="8e77a-122">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="8e77a-123">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="8e77a-123">VT\_UI4</span></span> | <span data-ttu-id="8e77a-124">Obbligatorio. il codice di risposta per il codice operativo del fornitore.</span><span class="sxs-lookup"><span data-stu-id="8e77a-124">Required.The response code to the vendor operation code.</span></span>                                                                                |
| <span data-ttu-id="8e77a-125">**\_Proprietà WPD \_ \_ parametri di \_ risposta MTP ext \_**</span><span class="sxs-lookup"><span data-stu-id="8e77a-125">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="8e77a-126">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="8e77a-126">VT\_UI4</span></span> | <span data-ttu-id="8e77a-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8e77a-127">Optional.</span></span> <span data-ttu-id="8e77a-128">Raccolta **IPortableDevicePropVariantCollection** che identifica eventuali parametri di risposta.</span><span class="sxs-lookup"><span data-stu-id="8e77a-128">An **IPortableDevicePropVariantCollection** collection that identifies any response parameters.</span></span> <span data-ttu-id="8e77a-129">Questa raccolta può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="8e77a-129">This collection can be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="8e77a-130">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="8e77a-130">Calling Methods</span></span>

<span data-ttu-id="8e77a-131">Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="8e77a-131">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e77a-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e77a-132">Requirements</span></span>



| <span data-ttu-id="8e77a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e77a-133">Requirement</span></span> | <span data-ttu-id="8e77a-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8e77a-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e77a-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e77a-135">Header</span></span><br/> | <dl> <span data-ttu-id="8e77a-136"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e77a-136"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e77a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e77a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e77a-138">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="8e77a-138">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

