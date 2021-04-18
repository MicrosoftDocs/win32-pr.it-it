---
description: Il \_ \_ comando di rimozione dell'archiviazione del comando WPD \_ espelle un supporto di archiviazione che può essere espulso in remoto dal computer.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: Comando WPD_COMMAND_STORAGE_EJECT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3eab2c6296b957b8edf1d65f21264cb93144aeb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330563"
---
# <a name="wpd_command_storage_eject-command"></a><span data-ttu-id="f35a0-103">\_Comando di \_ rimozione dell'archiviazione del comando WPD \_</span><span class="sxs-lookup"><span data-stu-id="f35a0-103">WPD\_COMMAND\_STORAGE\_EJECT Command</span></span>

<span data-ttu-id="f35a0-104">Il comando di **\_ rimozione dell' \_ archiviazione \_ del comando WPD** espelle un supporto di archiviazione che può essere espulso in remoto dal computer.</span><span class="sxs-lookup"><span data-stu-id="f35a0-104">The **WPD\_COMMAND\_STORAGE\_EJECT** command ejects a storage medium that can be ejected remotely by the computer.</span></span>

## <a name="command-category"></a><span data-ttu-id="f35a0-105">Categoria</span><span class="sxs-lookup"><span data-stu-id="f35a0-105">Command category</span></span>

<span data-ttu-id="f35a0-106">**\_archiviazione categoria \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f35a0-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="f35a0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f35a0-107">Parameters</span></span>

<span data-ttu-id="f35a0-108">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="f35a0-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="f35a0-109">Parametro</span><span class="sxs-lookup"><span data-stu-id="f35a0-109">Parameter</span></span>                          | <span data-ttu-id="f35a0-110">VarType</span><span class="sxs-lookup"><span data-stu-id="f35a0-110">VarType</span></span>    | <span data-ttu-id="f35a0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f35a0-111">Description</span></span>                                             |
|------------------------------------|------------|---------------------------------------------------------|
| <span data-ttu-id="f35a0-112">\_ \_ ID oggetto di archiviazione proprietà \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="f35a0-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="f35a0-113">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="f35a0-113">VT\_LPWSTR</span></span> | <span data-ttu-id="f35a0-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f35a0-114">Required.</span></span> <span data-ttu-id="f35a0-115">ID oggetto dell'oggetto di archiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f35a0-115">The object ID of the storage object to eject.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="f35a0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f35a0-116">Return Value</span></span>

<span data-ttu-id="f35a0-117">Il driver dovrebbe restituire i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="f35a0-117">The driver should return the following results.</span></span>



| <span data-ttu-id="f35a0-118">Risultato</span><span class="sxs-lookup"><span data-stu-id="f35a0-118">Result</span></span>                                         | <span data-ttu-id="f35a0-119">VarType</span><span class="sxs-lookup"><span data-stu-id="f35a0-119">VarType</span></span>   | <span data-ttu-id="f35a0-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f35a0-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f35a0-121">**\_ \_ HRESULT comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f35a0-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="f35a0-122">\_errore VT</span><span class="sxs-lookup"><span data-stu-id="f35a0-122">VT\_ERROR</span></span> | <span data-ttu-id="f35a0-123">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f35a0-123">Required.</span></span> <span data-ttu-id="f35a0-124">**HRESULT** che indica l'esito positivo o negativo dell'esecuzione del comando.</span><span class="sxs-lookup"><span data-stu-id="f35a0-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="f35a0-125">Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato.</span><span class="sxs-lookup"><span data-stu-id="f35a0-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="f35a0-126">I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati.</span><span class="sxs-lookup"><span data-stu-id="f35a0-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="f35a0-127">**\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f35a0-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="f35a0-128">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="f35a0-128">VT\_UI4</span></span>   | <span data-ttu-id="f35a0-129">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f35a0-129">Optional.</span></span> <span data-ttu-id="f35a0-130">Codice di errore specifico del driver.</span><span class="sxs-lookup"><span data-stu-id="f35a0-130">A driver-specific error code.</span></span> <span data-ttu-id="f35a0-131">Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.</span><span class="sxs-lookup"><span data-stu-id="f35a0-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="f35a0-132">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="f35a0-132">Calling Methods</span></span>

<span data-ttu-id="f35a0-133">Può essere chiamato solo direttamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="f35a0-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="f35a0-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f35a0-134">Requirements</span></span>



| <span data-ttu-id="f35a0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f35a0-135">Requirement</span></span> | <span data-ttu-id="f35a0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f35a0-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f35a0-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f35a0-137">Header</span></span><br/> | <dl> <span data-ttu-id="f35a0-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f35a0-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f35a0-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f35a0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f35a0-140">**Comandi**</span><span class="sxs-lookup"><span data-stu-id="f35a0-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




