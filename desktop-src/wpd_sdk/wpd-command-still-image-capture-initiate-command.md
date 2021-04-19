---
description: Il comando WPD il comando \_ \_ \_ \_ di avvio dell'acquisizione di immagini continua \_ ad avviare un'acquisizione di immagini ancora da parte di un oggetto funzionale per le immagini. Se viene creato un nuovo oggetto in seguito all'acquisizione di un'immagine, il driver deve inviare l' \_ evento WPD \_ aggiunto all'oggetto evento \_ .
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: Comando WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333618"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a><span data-ttu-id="37c8d-104">\_Comando di avvio del comando WPD \_ still \_ Image \_ Capture \_</span><span class="sxs-lookup"><span data-stu-id="37c8d-104">WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE Command</span></span>

<span data-ttu-id="37c8d-105">Il comando WPD il comando di **\_ avvio dell' \_ \_ \_ acquisizione \_ di immagini continua** ad avviare un'acquisizione di immagini ancora da parte di un oggetto funzionale per le immagini.</span><span class="sxs-lookup"><span data-stu-id="37c8d-105">The **WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE** command initiates a still image capture by a still image functional object.</span></span> <span data-ttu-id="37c8d-106">Se viene creato un nuovo oggetto in seguito all'acquisizione di un'immagine, il driver deve inviare l' **evento \_ WPD \_ \_ aggiunto all'oggetto evento** .</span><span class="sxs-lookup"><span data-stu-id="37c8d-106">If a new object is created as a result of taking a picture, the driver should send the **WPD\_EVENT\_OBJECT\_ADDED** event.</span></span>

## <a name="command-category"></a><span data-ttu-id="37c8d-107">Categoria</span><span class="sxs-lookup"><span data-stu-id="37c8d-107">Command category</span></span>

<span data-ttu-id="37c8d-108">**\_acquisizione di \_ \_ Immagini ancora della categoria \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="37c8d-108">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span>

## <a name="parameters"></a><span data-ttu-id="37c8d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="37c8d-109">Parameters</span></span>

<span data-ttu-id="37c8d-110">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="37c8d-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="37c8d-111">Parametro</span><span class="sxs-lookup"><span data-stu-id="37c8d-111">Parameter</span></span>                              | <span data-ttu-id="37c8d-112">VarType</span><span class="sxs-lookup"><span data-stu-id="37c8d-112">VarType</span></span>    | <span data-ttu-id="37c8d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37c8d-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c8d-114">\_ \_ \_ destinazione comando comune della proprietà WPD \_</span><span class="sxs-lookup"><span data-stu-id="37c8d-114">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="37c8d-115">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="37c8d-115">VT\_LPWSTR</span></span> | <span data-ttu-id="37c8d-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="37c8d-116">Required.</span></span> <span data-ttu-id="37c8d-117">ID oggetto dell'oggetto funzionale Acquisisci immagine ancora sul dispositivo che dovrebbe scattare l'immagine. Ogni oggetto funzionale Acquisisci immagine può avere impostazioni diverse e può fare riferimento a hardware diverso in un dispositivo (ad esempio, una fotocamera anteriore o posteriore di un telefono) e questo parametro indica quello da usare.</span><span class="sxs-lookup"><span data-stu-id="37c8d-117">The object ID of the still image capture functional object on the device that should take the picture.Each still image capture functional object can have different settings, and may refer to different hardware on a device (for example, a front or back camera of a phone), and this parameter indicates which one to use.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="37c8d-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37c8d-118">Return Value</span></span>

<span data-ttu-id="37c8d-119">Il driver dovrebbe restituire i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="37c8d-119">The driver should return the following results.</span></span>



| <span data-ttu-id="37c8d-120">Risultato</span><span class="sxs-lookup"><span data-stu-id="37c8d-120">Result</span></span>                                         | <span data-ttu-id="37c8d-121">VarType</span><span class="sxs-lookup"><span data-stu-id="37c8d-121">VarType</span></span>   | <span data-ttu-id="37c8d-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37c8d-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c8d-123">**\_ \_ HRESULT comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="37c8d-123">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="37c8d-124">\_errore VT</span><span class="sxs-lookup"><span data-stu-id="37c8d-124">VT\_ERROR</span></span> | <span data-ttu-id="37c8d-125">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="37c8d-125">Required.</span></span> <span data-ttu-id="37c8d-126">**HRESULT** che indica l'esito positivo o negativo dell'esecuzione del comando.</span><span class="sxs-lookup"><span data-stu-id="37c8d-126">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="37c8d-127">Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato.</span><span class="sxs-lookup"><span data-stu-id="37c8d-127">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="37c8d-128">I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati.</span><span class="sxs-lookup"><span data-stu-id="37c8d-128">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="37c8d-129">**\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="37c8d-129">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="37c8d-130">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="37c8d-130">VT\_UI4</span></span>   | <span data-ttu-id="37c8d-131">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="37c8d-131">Optional.</span></span> <span data-ttu-id="37c8d-132">Codice di errore specifico del driver.</span><span class="sxs-lookup"><span data-stu-id="37c8d-132">A driver-specific error code.</span></span> <span data-ttu-id="37c8d-133">Questo valore viene in genere usato dai fornitori di dispositivi per migliorare la diagnosi degli errori del dispositivo durante l'uso delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="37c8d-133">This value is typically used by device vendors to improve diagnosis of device errors while using their applications.</span></span> <span data-ttu-id="37c8d-134">Le applicazioni per utilizzo generico lo ignorano e si basano invece esclusivamente sulla proprietà WPD, \_ \_ \_ HRESULT comune.</span><span class="sxs-lookup"><span data-stu-id="37c8d-134">General purpose applications would ignore it and rely solely on WPD\_PROPERTY\_COMMON\_HRESULT instead.</span></span>                                                                                                                   |



 

## <a name="calling-methods"></a><span data-ttu-id="37c8d-135">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="37c8d-135">Calling Methods</span></span>

<span data-ttu-id="37c8d-136">Può essere chiamato solo direttamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="37c8d-136">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="37c8d-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37c8d-137">Requirements</span></span>



| <span data-ttu-id="37c8d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c8d-138">Requirement</span></span> | <span data-ttu-id="37c8d-139">Valore</span><span class="sxs-lookup"><span data-stu-id="37c8d-139">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c8d-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37c8d-140">Header</span></span><br/> | <dl> <span data-ttu-id="37c8d-141"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="37c8d-141"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37c8d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37c8d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c8d-143">**Comandi**</span><span class="sxs-lookup"><span data-stu-id="37c8d-143">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




