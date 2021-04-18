---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ get \_ supported \_ Vendor \_ OpCodes Invia un blocco di comandi MTP. A questo comando non è associata alcuna fase di dati successiva.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: Comando WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330575"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a><span data-ttu-id="d278b-104">\_Comando WPD \_ MTP \_ ext \_ get \_ supported \_ Vendor \_ OpCodes</span><span class="sxs-lookup"><span data-stu-id="d278b-104">WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES Command</span></span>

<span data-ttu-id="d278b-105">Il comando **WPD \_ comando \_ MTP \_ ext \_ get \_ supported \_ Vendor \_ OpCodes** Invia un blocco di comandi MTP.</span><span class="sxs-lookup"><span data-stu-id="d278b-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES** command sends an MTP command block.</span></span> <span data-ttu-id="d278b-106">A questo comando non è associata alcuna fase di dati successiva.</span><span class="sxs-lookup"><span data-stu-id="d278b-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="d278b-107">Categoria</span><span class="sxs-lookup"><span data-stu-id="d278b-107">Command category</span></span>

<span data-ttu-id="d278b-108">**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="d278b-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="d278b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d278b-109">Parameters</span></span>

<span data-ttu-id="d278b-110">Questo comando non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="d278b-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d278b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d278b-111">Return Value</span></span>

<span data-ttu-id="d278b-112">Il driver restituisce i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="d278b-112">The driver returns the following results.</span></span>



| <span data-ttu-id="d278b-113">Risultato</span><span class="sxs-lookup"><span data-stu-id="d278b-113">Result</span></span>                                                | <span data-ttu-id="d278b-114">VarType</span><span class="sxs-lookup"><span data-stu-id="d278b-114">VarType</span></span> | <span data-ttu-id="d278b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d278b-115">Description</span></span>                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d278b-116">**WPD \_ proprietà \_ MTP \_ \_ \_ codici operazione fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="d278b-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_OPERATION\_CODES**</span></span> | <span data-ttu-id="d278b-117">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="d278b-117">VT\_UI4</span></span> | <span data-ttu-id="d278b-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d278b-118">Required.</span></span> <span data-ttu-id="d278b-119">Oggetto **IPortableDevicePropVariantCollection** che contiene tutti i codici operativi estesi del fornitore.</span><span class="sxs-lookup"><span data-stu-id="d278b-119">An **IPortableDevicePropVariantCollection** that contains all vendor-extended operation codes.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="d278b-120">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="d278b-120">Calling Methods</span></span>

<span data-ttu-id="d278b-121">Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="d278b-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="d278b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d278b-122">Requirements</span></span>



| <span data-ttu-id="d278b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d278b-123">Requirement</span></span> | <span data-ttu-id="d278b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d278b-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d278b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d278b-125">Header</span></span><br/> | <dl> <span data-ttu-id="d278b-126"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="d278b-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d278b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d278b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d278b-128">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="d278b-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




