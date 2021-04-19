---
description: Il comando \_ \_ SMS \_ Send di WPD avvia l'invio di un messaggio SMS (Short Message Service) da un oggetto funzionale SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: Comando WPD_COMMAND_SMS_SEND (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325940"
---
# <a name="wpd_command_sms_send-command"></a><span data-ttu-id="2c90b-103">\_Comando di \_ invio SMS di comando WPD \_</span><span class="sxs-lookup"><span data-stu-id="2c90b-103">WPD\_COMMAND\_SMS\_SEND Command</span></span>

<span data-ttu-id="2c90b-104">Il **comando \_ \_ SMS \_ Send di WPD** avvia l'invio di un messaggio SMS (Short Message Service) da un oggetto funzionale SMS.</span><span class="sxs-lookup"><span data-stu-id="2c90b-104">The **WPD\_COMMAND\_SMS\_SEND** command initiates the sending of a short message service (SMS) message by an SMS functional object.</span></span>

## <a name="command-category"></a><span data-ttu-id="2c90b-105">Categoria</span><span class="sxs-lookup"><span data-stu-id="2c90b-105">Command category</span></span>

<span data-ttu-id="2c90b-106">**\_SMS della categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2c90b-106">**WPD\_CATEGORY\_SMS**</span></span>

## <a name="parameters"></a><span data-ttu-id="2c90b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c90b-107">Parameters</span></span>

<span data-ttu-id="2c90b-108">Per il driver sono previsti i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c90b-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="2c90b-109">Parametro</span><span class="sxs-lookup"><span data-stu-id="2c90b-109">Parameter</span></span>                              | <span data-ttu-id="2c90b-110">VarType</span><span class="sxs-lookup"><span data-stu-id="2c90b-110">VarType</span></span>             | <span data-ttu-id="2c90b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c90b-111">Description</span></span>                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c90b-112">\_ \_ \_ destinazione comando comune della proprietà WPD \_</span><span class="sxs-lookup"><span data-stu-id="2c90b-112">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="2c90b-113">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="2c90b-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="2c90b-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c90b-114">Required.</span></span> <span data-ttu-id="2c90b-115">ID oggetto dell'oggetto funzionale SMS che deve inviare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="2c90b-115">The object ID of the SMS functional object that should send the message.</span></span> <span data-ttu-id="2c90b-116">Diversi oggetti funzionali SMS possono avere impostazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="2c90b-116">Different SMS functional objects can have different settings.</span></span>                                                                                     |
| <span data-ttu-id="2c90b-117">\_ \_ destinatario SMS della proprietà WPD \_</span><span class="sxs-lookup"><span data-stu-id="2c90b-117">WPD\_PROPERTY\_SMS\_RECIPIENT</span></span>          | <span data-ttu-id="2c90b-118">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="2c90b-118">VT\_LPWSTR</span></span>          | <span data-ttu-id="2c90b-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c90b-119">Required.</span></span> <span data-ttu-id="2c90b-120">URI del destinatario.</span><span class="sxs-lookup"><span data-stu-id="2c90b-120">The URI of the recipient.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="2c90b-121">\_tipo di \_ \_ messaggio SMS della proprietà \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2c90b-121">WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE</span></span>      | <span data-ttu-id="2c90b-122">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="2c90b-122">VT\_UI4</span></span>             | <span data-ttu-id="2c90b-123">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c90b-123">Required.</span></span> <span data-ttu-id="2c90b-124">Enumeratore dei [**\_ \_ tipi di messaggio SMS**](sms-message-types.md) che indica il tipo di messaggio (testo o binario).</span><span class="sxs-lookup"><span data-stu-id="2c90b-124">An [**SMS\_MESSAGE\_TYPES**](sms-message-types.md) enumerator that indicates the type of message (text or binary).</span></span>                                                                                                        |
| <span data-ttu-id="2c90b-125">\_messaggio di \_ \_ testo SMS della proprietà \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2c90b-125">WPD\_PROPERTY\_SMS\_TEXT\_MESSAGE</span></span>      | <span data-ttu-id="2c90b-126">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="2c90b-126">VT\_LPWSTR</span></span>          | <span data-ttu-id="2c90b-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2c90b-127">Optional.</span></span> <span data-ttu-id="2c90b-128">Se **il \_ \_ tipo di \_ messaggio \_ SMS della proprietà WPD** indica un messaggio di testo, si tratta della stringa del messaggio; in caso contrario, questo parametro non è incluso.</span><span class="sxs-lookup"><span data-stu-id="2c90b-128">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a text message, this is the message string; otherwise, this parameter is not included.</span></span>                                                                                  |
| <span data-ttu-id="2c90b-129">\_ \_ \_ messaggio binario SMS proprietà \_ WPD</span><span class="sxs-lookup"><span data-stu-id="2c90b-129">WPD\_PROPERTY\_SMS\_BINARY\_MESSAGE</span></span>    | <span data-ttu-id="2c90b-130">VT \_ vettore \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="2c90b-130">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="2c90b-131">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2c90b-131">Optional.</span></span> <span data-ttu-id="2c90b-132">Se **il \_ \_ tipo di \_ messaggio \_ SMS della proprietà WPD** indica un messaggio binario, si tratta di un puntatore a una matrice di byte. in caso contrario, questo parametro non è incluso.</span><span class="sxs-lookup"><span data-stu-id="2c90b-132">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a binary message, this is a pointer to an array of bytes; otherwise, this parameter is not included.</span></span> <span data-ttu-id="2c90b-133">Il primo valore DWORD del valore è la lunghezza della matrice in byte.</span><span class="sxs-lookup"><span data-stu-id="2c90b-133">The first DWORD of the value is the length of the array, in bytes.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="2c90b-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c90b-134">Return Value</span></span>

<span data-ttu-id="2c90b-135">Il driver dovrebbe restituire i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c90b-135">The driver should return the following results.</span></span>



| <span data-ttu-id="2c90b-136">Risultato</span><span class="sxs-lookup"><span data-stu-id="2c90b-136">Result</span></span>                                         | <span data-ttu-id="2c90b-137">VarType</span><span class="sxs-lookup"><span data-stu-id="2c90b-137">VarType</span></span>   | <span data-ttu-id="2c90b-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c90b-138">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c90b-139">**\_ \_ HRESULT comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2c90b-139">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="2c90b-140">\_errore VT</span><span class="sxs-lookup"><span data-stu-id="2c90b-140">VT\_ERROR</span></span> | <span data-ttu-id="2c90b-141">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c90b-141">Required.</span></span> <span data-ttu-id="2c90b-142">**HRESULT** che indica l'esito positivo o negativo dell'esecuzione del comando.</span><span class="sxs-lookup"><span data-stu-id="2c90b-142">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="2c90b-143">Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato.</span><span class="sxs-lookup"><span data-stu-id="2c90b-143">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="2c90b-144">I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati.</span><span class="sxs-lookup"><span data-stu-id="2c90b-144">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="2c90b-145">**\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2c90b-145">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="2c90b-146">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="2c90b-146">VT\_UI4</span></span>   | <span data-ttu-id="2c90b-147">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2c90b-147">Optional.</span></span> <span data-ttu-id="2c90b-148">Codice di errore specifico del driver.</span><span class="sxs-lookup"><span data-stu-id="2c90b-148">A driver-specific error code.</span></span> <span data-ttu-id="2c90b-149">Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.</span><span class="sxs-lookup"><span data-stu-id="2c90b-149">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="2c90b-150">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="2c90b-150">Calling Methods</span></span>

<span data-ttu-id="2c90b-151">Può essere chiamato solo direttamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="2c90b-151">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c90b-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c90b-152">Requirements</span></span>



| <span data-ttu-id="2c90b-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c90b-153">Requirement</span></span> | <span data-ttu-id="2c90b-154">Valore</span><span class="sxs-lookup"><span data-stu-id="2c90b-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c90b-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c90b-155">Header</span></span><br/> | <dl> <span data-ttu-id="2c90b-156"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c90b-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c90b-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c90b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c90b-158">**Comandi**</span><span class="sxs-lookup"><span data-stu-id="2c90b-158">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




