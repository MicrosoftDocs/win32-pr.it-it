---
description: Il \_ comando WPD comando \_ MTP \_ ext \_ get \_ Vendor \_ Extension \_ Description recupera la stringa di descrizione Vendor-Extension. Questa stringa è definita da un set di dati DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: Comando WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330569"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a><span data-ttu-id="5fd7c-104">\_Comando WPD \_ MTP \_ ext \_ get \_ Vendor \_ Extension \_ Description</span><span class="sxs-lookup"><span data-stu-id="5fd7c-104">WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION Command</span></span>

<span data-ttu-id="5fd7c-105">Il comando **WPD \_ comando \_ MTP \_ ext \_ get \_ Vendor \_ Extension \_ Description** recupera la stringa di descrizione Vendor-Extension.</span><span class="sxs-lookup"><span data-stu-id="5fd7c-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION** command retrieves the vendor-extension description string.</span></span> <span data-ttu-id="5fd7c-106">Questa stringa è definita da un set di dati **deviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="5fd7c-106">This string is defined by a **DeviceInfo** dataset.</span></span>

## <a name="command-category"></a><span data-ttu-id="5fd7c-107">Categoria</span><span class="sxs-lookup"><span data-stu-id="5fd7c-107">Command category</span></span>

<span data-ttu-id="5fd7c-108">**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**</span><span class="sxs-lookup"><span data-stu-id="5fd7c-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="5fd7c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fd7c-109">Parameters</span></span>

<span data-ttu-id="5fd7c-110">Questo comando non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="5fd7c-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5fd7c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fd7c-111">Return Value</span></span>

<span data-ttu-id="5fd7c-112">Il driver restituisce i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="5fd7c-112">The driver returns the following results.</span></span>



| <span data-ttu-id="5fd7c-113">Risultato</span><span class="sxs-lookup"><span data-stu-id="5fd7c-113">Result</span></span>                                                      | <span data-ttu-id="5fd7c-114">VarType</span><span class="sxs-lookup"><span data-stu-id="5fd7c-114">VarType</span></span>    | <span data-ttu-id="5fd7c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fd7c-115">Description</span></span>                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| <span data-ttu-id="5fd7c-116">**\_Proprietà WPD \_ \_ \_ \_ Descrizione estensione fornitore ext \_**</span><span class="sxs-lookup"><span data-stu-id="5fd7c-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_EXTENSION\_DESCRIPTION**</span></span> | <span data-ttu-id="5fd7c-117">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="5fd7c-117">VT\_LPWSTR</span></span> | <span data-ttu-id="5fd7c-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fd7c-118">Required.</span></span> <span data-ttu-id="5fd7c-119">Specifica la stringa di descrizione dell'estensione del fornitore.</span><span class="sxs-lookup"><span data-stu-id="5fd7c-119">Specifies the vendor-extension description string.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="5fd7c-120">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="5fd7c-120">Calling Methods</span></span>

<span data-ttu-id="5fd7c-121">Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="5fd7c-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd7c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fd7c-122">Requirements</span></span>



| <span data-ttu-id="5fd7c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd7c-123">Requirement</span></span> | <span data-ttu-id="5fd7c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5fd7c-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd7c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fd7c-125">Header</span></span><br/> | <dl> <span data-ttu-id="5fd7c-126"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd7c-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd7c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fd7c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd7c-128">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="5fd7c-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




