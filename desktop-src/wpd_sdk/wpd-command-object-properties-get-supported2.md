---
description: Recupera le proprietà supportate da un oggetto.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: Comando WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330564"
---
# <a name="wpd_command_object_properties_get_supported-command"></a><span data-ttu-id="1ae75-103">\_Comando WPD \_ Proprietà oggetto comando \_ \_ get \_ supported</span><span class="sxs-lookup"><span data-stu-id="1ae75-103">WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED Command</span></span>

<span data-ttu-id="1ae75-104">Il **comando \_ WPD \_ Proprietà oggetto comando \_ \_ get \_ supported** recupera le proprietà supportate da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1ae75-104">The **WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED** command retrieves the properties supported by an object.</span></span>

## <a name="command-category"></a><span data-ttu-id="1ae75-105">Categoria comando</span><span class="sxs-lookup"><span data-stu-id="1ae75-105">Command Category</span></span>

<span data-ttu-id="1ae75-106">**\_proprietà dell' \_ oggetto \_ categoria WPD**</span><span class="sxs-lookup"><span data-stu-id="1ae75-106">**WPD\_CATEGORY\_OBJECT\_PROPERTIES**</span></span>

## <a name="parameters"></a><span data-ttu-id="1ae75-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ae75-107">Parameters</span></span>

<span data-ttu-id="1ae75-108">Il driver prevede il seguente parametro.</span><span class="sxs-lookup"><span data-stu-id="1ae75-108">The driver expects the following parameter.</span></span>



| <span data-ttu-id="1ae75-109">Parametro</span><span class="sxs-lookup"><span data-stu-id="1ae75-109">Parameter</span></span>                                         | <span data-ttu-id="1ae75-110">VarType</span><span class="sxs-lookup"><span data-stu-id="1ae75-110">VarType</span></span>        | <span data-ttu-id="1ae75-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ae75-111">Description</span></span>                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="1ae75-112">**\_ \_ \_ \_ ID oggetto proprietà oggetto proprietà \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1ae75-112">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_OBJECT\_ID**</span></span> | <span data-ttu-id="1ae75-113">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="1ae75-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1ae75-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ae75-114">Required.</span></span> <span data-ttu-id="1ae75-115">ID dell'oggetto che contiene le proprietà richieste.</span><span class="sxs-lookup"><span data-stu-id="1ae75-115">The ID of the object that contains the requested properties.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="1ae75-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ae75-116">Return Value</span></span>

<span data-ttu-id="1ae75-117">Il driver dovrebbe restituire i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ae75-117">The driver should return the following results.</span></span>



| <span data-ttu-id="1ae75-118">Risultato</span><span class="sxs-lookup"><span data-stu-id="1ae75-118">Result</span></span>                                                | <span data-ttu-id="1ae75-119">VarType</span><span class="sxs-lookup"><span data-stu-id="1ae75-119">VarType</span></span>         | <span data-ttu-id="1ae75-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ae75-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae75-121">**proprietà \_ \_ oggetto proprietà \_ WPD \_ \_ chiavi proprietà**</span><span class="sxs-lookup"><span data-stu-id="1ae75-121">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_PROPERTY\_KEYS**</span></span> | <span data-ttu-id="1ae75-122">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="1ae75-122">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="1ae75-123">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ae75-123">Required.</span></span> <span data-ttu-id="1ae75-124">Interfaccia [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che specifica tutte le proprietà supportate.</span><span class="sxs-lookup"><span data-stu-id="1ae75-124">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that specifies all of the supported properties.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="1ae75-125">**\_ \_ HRESULT comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1ae75-125">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                    | <span data-ttu-id="1ae75-126">**\_errore VT**</span><span class="sxs-lookup"><span data-stu-id="1ae75-126">**VT\_ERROR**</span></span>   | <span data-ttu-id="1ae75-127">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ae75-127">Required.</span></span> <span data-ttu-id="1ae75-128">Valore **HRESULT** che indica l'esito positivo o negativo complessivo.</span><span class="sxs-lookup"><span data-stu-id="1ae75-128">An **HRESULT** value that indicates overall success or failure.</span></span> <span data-ttu-id="1ae75-129">I possibili valori dei risultati includono i [codici di errore dei dispositivi portatili Windows](error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1ae75-129">Possible result values include [Windows Portable Devices error codes](error-constants.md).</span></span> <span data-ttu-id="1ae75-130">Se il chiamante esegue una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** , ma in caso contrario non è necessario per restituire altri valori di risultato.</span><span class="sxs-lookup"><span data-stu-id="1ae75-130">If the caller makes an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** but is otherwise not required to return any other result value.</span></span> |
| <span data-ttu-id="1ae75-131">**\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1ae75-131">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>        | <span data-ttu-id="1ae75-132">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1ae75-132">**VT\_UI4**</span></span>     | <span data-ttu-id="1ae75-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1ae75-133">Optional.</span></span> <span data-ttu-id="1ae75-134">Codice di errore specifico del driver.</span><span class="sxs-lookup"><span data-stu-id="1ae75-134">A driver-specific error code.</span></span> <span data-ttu-id="1ae75-135">Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.</span><span class="sxs-lookup"><span data-stu-id="1ae75-135">This is typically used only for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="1ae75-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ae75-136">Requirements</span></span>



| <span data-ttu-id="1ae75-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae75-137">Requirement</span></span> | <span data-ttu-id="1ae75-138">Valore</span><span class="sxs-lookup"><span data-stu-id="1ae75-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae75-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ae75-139">Header</span></span><br/> | <dl> <span data-ttu-id="1ae75-140"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae75-140"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ae75-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ae75-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae75-142">**Comandi**</span><span class="sxs-lookup"><span data-stu-id="1ae75-142">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




