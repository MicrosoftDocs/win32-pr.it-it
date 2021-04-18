---
description: Il \_ comando WPD Command \_ storage \_ format formatta un oggetto funzionale di archiviazione nel dispositivo.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: Comando WPD_COMMAND_STORAGE_FORMAT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330562"
---
# <a name="wpd_command_storage_format-command"></a><span data-ttu-id="f6a0b-103">\_Comando WPD Command \_ storage \_ Format</span><span class="sxs-lookup"><span data-stu-id="f6a0b-103">WPD\_COMMAND\_STORAGE\_FORMAT Command</span></span>

<span data-ttu-id="f6a0b-104">Il comando **WPD \_ Command \_ storage \_ Format** formatta un oggetto funzionale di archiviazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-104">The **WPD\_COMMAND\_STORAGE\_FORMAT** command formats a storage functional object on the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="f6a0b-105">Categoria</span><span class="sxs-lookup"><span data-stu-id="f6a0b-105">Command category</span></span>

<span data-ttu-id="f6a0b-106">**\_archiviazione categoria \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f6a0b-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="f6a0b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6a0b-107">Parameters</span></span>

<span data-ttu-id="f6a0b-108">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="f6a0b-109">Parametro</span><span class="sxs-lookup"><span data-stu-id="f6a0b-109">Parameter</span></span>                          | <span data-ttu-id="f6a0b-110">VarType</span><span class="sxs-lookup"><span data-stu-id="f6a0b-110">VarType</span></span>    | <span data-ttu-id="f6a0b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6a0b-111">Description</span></span>                                              |
|------------------------------------|------------|----------------------------------------------------------|
| <span data-ttu-id="f6a0b-112">\_ \_ ID oggetto di archiviazione proprietà \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="f6a0b-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="f6a0b-113">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="f6a0b-113">VT\_LPWSTR</span></span> | <span data-ttu-id="f6a0b-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-114">Required.</span></span> <span data-ttu-id="f6a0b-115">ID oggetto del supporto di archiviazione da formattare.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-115">The object ID of the storage medium to format.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="f6a0b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6a0b-116">Return Value</span></span>

<span data-ttu-id="f6a0b-117">Il driver dovrebbe restituire i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-117">The driver should return the following results.</span></span>



| <span data-ttu-id="f6a0b-118">Risultato</span><span class="sxs-lookup"><span data-stu-id="f6a0b-118">Result</span></span>                                         | <span data-ttu-id="f6a0b-119">VarType</span><span class="sxs-lookup"><span data-stu-id="f6a0b-119">VarType</span></span>   | <span data-ttu-id="f6a0b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6a0b-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a0b-121">**\_ \_ HRESULT comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f6a0b-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="f6a0b-122">\_errore VT</span><span class="sxs-lookup"><span data-stu-id="f6a0b-122">VT\_ERROR</span></span> | <span data-ttu-id="f6a0b-123">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-123">Required.</span></span> <span data-ttu-id="f6a0b-124">**HRESULT** che indica l'esito positivo o negativo dell'esecuzione del comando.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="f6a0b-125">Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="f6a0b-126">I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="f6a0b-127">**\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f6a0b-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="f6a0b-128">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="f6a0b-128">VT\_UI4</span></span>   | <span data-ttu-id="f6a0b-129">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-129">Optional.</span></span> <span data-ttu-id="f6a0b-130">Codice di errore specifico del driver.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-130">A driver-specific error code.</span></span> <span data-ttu-id="f6a0b-131">Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.</span><span class="sxs-lookup"><span data-stu-id="f6a0b-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="f6a0b-132">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="f6a0b-132">Calling Methods</span></span>

<span data-ttu-id="f6a0b-133">Può essere chiamato solo direttamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="f6a0b-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a0b-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6a0b-134">Requirements</span></span>



| <span data-ttu-id="f6a0b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6a0b-135">Requirement</span></span> | <span data-ttu-id="f6a0b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f6a0b-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a0b-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6a0b-137">Header</span></span><br/> | <dl> <span data-ttu-id="f6a0b-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6a0b-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6a0b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6a0b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a0b-140">**Comandi**</span><span class="sxs-lookup"><span data-stu-id="f6a0b-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




