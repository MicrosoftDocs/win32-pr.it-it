---
description: Il \_ comando WPD comando \_ Device \_ hint \_ get \_ Content \_ percorso recupera gli ID oggetto delle cartelle che possono ospitare un oggetto di un tipo specificato.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: Comando WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324805"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a><span data-ttu-id="124fe-103">\_Comando WPD comando per ottenere il \_ \_ \_ \_ percorso del contenuto \_</span><span class="sxs-lookup"><span data-stu-id="124fe-103">WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION Command</span></span>

<span data-ttu-id="124fe-104">Il comando **WPD \_ comando \_ Device \_ hint \_ get \_ Content \_ percorso** recupera gli ID oggetto delle cartelle che possono ospitare un oggetto di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="124fe-104">The **WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION** command retrieves the object IDs of folders that can hold an object of a specified type.</span></span> <span data-ttu-id="124fe-105">Questo comando viene fornito come modo più rapido per un client di individuare la posizione in cui un dispositivo Archivia oggetti specifici rispetto all'enumerazione di oggetti bruti.</span><span class="sxs-lookup"><span data-stu-id="124fe-105">This command is provided as a faster way for a client to discover where a device stores specific objects than by brute object enumeration.</span></span>

## <a name="command-category"></a><span data-ttu-id="124fe-106">Categoria</span><span class="sxs-lookup"><span data-stu-id="124fe-106">Command category</span></span>

<span data-ttu-id="124fe-107">**\_hint per \_ dispositivi di categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="124fe-107">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>

## <a name="parameters"></a><span data-ttu-id="124fe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="124fe-108">Parameters</span></span>

<span data-ttu-id="124fe-109">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="124fe-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="124fe-110">Parametro</span><span class="sxs-lookup"><span data-stu-id="124fe-110">Parameter</span></span>                                   | <span data-ttu-id="124fe-111">VarType</span><span class="sxs-lookup"><span data-stu-id="124fe-111">VarType</span></span>   | <span data-ttu-id="124fe-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="124fe-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="124fe-113">\_tipo di \_ \_ contenuto hint \_ del dispositivo della proprietà WPD \_</span><span class="sxs-lookup"><span data-stu-id="124fe-113">WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_TYPE</span></span> | <span data-ttu-id="124fe-114">\_CLSID VT</span><span class="sxs-lookup"><span data-stu-id="124fe-114">VT\_CLSID</span></span> | <span data-ttu-id="124fe-115">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="124fe-115">Required.</span></span> <span data-ttu-id="124fe-116">Il tipo di oggetto per il quale il chiamante desidera trovare il contenitore.</span><span class="sxs-lookup"><span data-stu-id="124fe-116">The object type that the caller wishes to find the container for.</span></span> <span data-ttu-id="124fe-117">Per trovare, ad esempio, le cartelle di primo livello usate per conservare le immagini in una fotocamera digitale, il chiamante invia l' \_ immagine del tipo di contenuto WPD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="124fe-117">For example, to find the top-level folders used to hold images on a digital camera, the caller would submit WPD\_CONTENT\_TYPE\_IMAGE.</span></span> <span data-ttu-id="124fe-118">Vedere [requisiti per gli oggetti](requirements-for-objects.md) per un elenco di tipi di oggetto definiti da dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="124fe-118">See [Requirements for Objects](requirements-for-objects.md) for a list of object types defined by Windows Portable Devices.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="124fe-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="124fe-119">Return Value</span></span>

<span data-ttu-id="124fe-120">Il driver dovrebbe restituire i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="124fe-120">The driver should return the following results.</span></span>



| <span data-ttu-id="124fe-121">Risultato</span><span class="sxs-lookup"><span data-stu-id="124fe-121">Result</span></span>                                               | <span data-ttu-id="124fe-122">VarType</span><span class="sxs-lookup"><span data-stu-id="124fe-122">VarType</span></span>     | <span data-ttu-id="124fe-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="124fe-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="124fe-124">**\_ \_ \_ \_ percorsi contenuto suggerimenti dispositivo proprietà \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="124fe-124">**WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_LOCATIONS**</span></span> | <span data-ttu-id="124fe-125">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="124fe-125">VT\_UNKNOWN</span></span> | <span data-ttu-id="124fe-126">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="124fe-126">Required.</span></span> <span data-ttu-id="124fe-127">Un [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo VT \_ LPWSTR valori che specificano gli ID oggetto delle cartelle contenenti oggetti del tipo indicato dal parametro chiamante.</span><span class="sxs-lookup"><span data-stu-id="124fe-127">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) of type VT\_LPWSTR values that specify the object IDs of folders containing objects of the type indicated by the calling parameter.</span></span> <span data-ttu-id="124fe-128">Se non viene trovata alcuna cartella, deve essere un elenco vuoto. Le cartelle indicate dal risultato possono contenere o meno oggetti di altri tipi di contenuto.</span><span class="sxs-lookup"><span data-stu-id="124fe-128">If no folders are found, this should be an empty list.The folders indicated by the result may or may not contain objects of other content types.</span></span> <span data-ttu-id="124fe-129">Per informazioni sulle restrizioni delle cartelle, vedere la proprietà [ \_ tipi di contenuto della cartella WPD \_ \_ \_ consentiti](miscellaneous-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="124fe-129">See the [WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED](miscellaneous-properties.md) property for information on folder restrictions.</span></span><br/> |
| <span data-ttu-id="124fe-130">**\_ \_ HRESULT comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="124fe-130">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                   | <span data-ttu-id="124fe-131">\_errore VT</span><span class="sxs-lookup"><span data-stu-id="124fe-131">VT\_ERROR</span></span>   | <span data-ttu-id="124fe-132">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="124fe-132">Required.</span></span> <span data-ttu-id="124fe-133">**HRESULT** che indica l'esito positivo o negativo della gestione del comando.</span><span class="sxs-lookup"><span data-stu-id="124fe-133">An **HRESULT** that indicates success or failure of handling the command.</span></span> <span data-ttu-id="124fe-134">Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato.</span><span class="sxs-lookup"><span data-stu-id="124fe-134">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="124fe-135">I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati.</span><span class="sxs-lookup"><span data-stu-id="124fe-135">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="124fe-136">**\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="124fe-136">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>       | <span data-ttu-id="124fe-137">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="124fe-137">VT\_UI4</span></span>     | <span data-ttu-id="124fe-138">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="124fe-138">Optional.</span></span> <span data-ttu-id="124fe-139">Codice di errore specifico del driver.</span><span class="sxs-lookup"><span data-stu-id="124fe-139">A driver-specific error code.</span></span> <span data-ttu-id="124fe-140">Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.</span><span class="sxs-lookup"><span data-stu-id="124fe-140">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a><span data-ttu-id="124fe-141">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="124fe-141">Calling Methods</span></span>

<span data-ttu-id="124fe-142">Può essere chiamato solo direttamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="124fe-142">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="124fe-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="124fe-143">Requirements</span></span>



| <span data-ttu-id="124fe-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="124fe-144">Requirement</span></span> | <span data-ttu-id="124fe-145">Valore</span><span class="sxs-lookup"><span data-stu-id="124fe-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="124fe-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="124fe-146">Header</span></span><br/> | <dl> <span data-ttu-id="124fe-147"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="124fe-147"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




