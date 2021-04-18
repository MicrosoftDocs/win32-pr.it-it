---
description: Il \_ comando WPD \_ Common \_ Reset \_ Device Reimposta il dispositivo. Questa operazione non significa riformattazione; equivale a spegnere e riaccendere il dispositivo.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: Comando WPD_COMMAND_COMMON_RESET_DEVICE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333736"
---
# <a name="wpd_command_common_reset_device-command"></a><span data-ttu-id="c72f1-104">\_Comando WPD \_ Common \_ Reset \_ Device comando</span><span class="sxs-lookup"><span data-stu-id="c72f1-104">WPD\_COMMAND\_COMMON\_RESET\_DEVICE Command</span></span>

<span data-ttu-id="c72f1-105">Il **comando \_ WPD \_ Common \_ Reset \_ Device Reimposta** il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c72f1-105">The **WPD\_COMMAND\_COMMON\_RESET\_DEVICE** command resets the device.</span></span> <span data-ttu-id="c72f1-106">Questa operazione non significa riformattazione; equivale a spegnere e riaccendere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c72f1-106">This does not mean reformatting; it is equivalent to turning the device off and on again.</span></span>

## <a name="command-category"></a><span data-ttu-id="c72f1-107">Categoria</span><span class="sxs-lookup"><span data-stu-id="c72f1-107">Command category</span></span>

<span data-ttu-id="c72f1-108">**\_categoria WPD \_ comune**</span><span class="sxs-lookup"><span data-stu-id="c72f1-108">**WPD\_CATEGORY\_COMMON**</span></span>

## <a name="parameters"></a><span data-ttu-id="c72f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c72f1-109">Parameters</span></span>

<span data-ttu-id="c72f1-110">Questo comando non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="c72f1-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c72f1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c72f1-111">Return Value</span></span>

<span data-ttu-id="c72f1-112">Il driver dovrebbe restituire i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="c72f1-112">The driver should return the following results.</span></span>



| <span data-ttu-id="c72f1-113">Risultato</span><span class="sxs-lookup"><span data-stu-id="c72f1-113">Result</span></span>                                         | <span data-ttu-id="c72f1-114">VarType</span><span class="sxs-lookup"><span data-stu-id="c72f1-114">VarType</span></span>   | <span data-ttu-id="c72f1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c72f1-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c72f1-116">**\_ \_ HRESULT comune della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c72f1-116">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="c72f1-117">\_errore VT</span><span class="sxs-lookup"><span data-stu-id="c72f1-117">VT\_ERROR</span></span> | <span data-ttu-id="c72f1-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c72f1-118">Required.</span></span> <span data-ttu-id="c72f1-119">**HRESULT** che indica l'esito positivo o negativo dell'esecuzione del comando.</span><span class="sxs-lookup"><span data-stu-id="c72f1-119">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="c72f1-120">Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato.</span><span class="sxs-lookup"><span data-stu-id="c72f1-120">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="c72f1-121">I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati.</span><span class="sxs-lookup"><span data-stu-id="c72f1-121">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="c72f1-122">**\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c72f1-122">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="c72f1-123">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="c72f1-123">VT\_UI4</span></span>   | <span data-ttu-id="c72f1-124">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c72f1-124">Optional.</span></span> <span data-ttu-id="c72f1-125">Codice di errore specifico del driver.</span><span class="sxs-lookup"><span data-stu-id="c72f1-125">A driver-specific error code.</span></span> <span data-ttu-id="c72f1-126">Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.</span><span class="sxs-lookup"><span data-stu-id="c72f1-126">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="c72f1-127">Chiamata di metodi</span><span class="sxs-lookup"><span data-stu-id="c72f1-127">Calling Methods</span></span>

<span data-ttu-id="c72f1-128">Può essere chiamato solo direttamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="c72f1-128">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="c72f1-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c72f1-129">Requirements</span></span>



| <span data-ttu-id="c72f1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c72f1-130">Requirement</span></span> | <span data-ttu-id="c72f1-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c72f1-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c72f1-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c72f1-132">Header</span></span><br/> | <dl> <span data-ttu-id="c72f1-133"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c72f1-133"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c72f1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c72f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72f1-135">**Comandi**</span><span class="sxs-lookup"><span data-stu-id="c72f1-135">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




