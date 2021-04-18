---
description: L'interfaccia ITAudioDeviceControl espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interfaccia ITAudioDeviceControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331905"
---
# <a name="itaudiodevicecontrol-interface"></a><span data-ttu-id="a9fc6-103">Interfaccia ITAudioDeviceControl</span><span class="sxs-lookup"><span data-stu-id="a9fc6-103">ITAudioDeviceControl interface</span></span>

<span data-ttu-id="a9fc6-104">\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a9fc6-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a9fc6-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a9fc6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a9fc6-106">L'interfaccia **ITAudioDeviceControl** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="a9fc6-106">The **ITAudioDeviceControl** interface exposes methods that enable an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="a9fc6-107">Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) e [H323 msp](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc6-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="a9fc6-108">Viene esposto quando una chiamata utilizza questi provider di servizi o un provider di servizi di terze parti che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a9fc6-108">It is exposed when a call uses these service providers or a third party service provider that implements this interface.</span></span> <span data-ttu-id="a9fc6-109">Per ottenere un puntatore all'interfaccia **ITAudioDeviceControl** , chiamare **QueryInterface** sull'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) che controlla il dispositivo audio corrispondente al flusso.</span><span class="sxs-lookup"><span data-stu-id="a9fc6-109">To obtain a pointer to the **ITAudioDeviceControl** interface, call **QueryInterface** on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface that controls the audio device corresponding to the stream.</span></span> <span data-ttu-id="a9fc6-110">Il tipo di supporto dell'interfaccia **ITStream** deve essere audio per l'esposizione dell'interfaccia **ITAudioDeviceControl** .</span><span class="sxs-lookup"><span data-stu-id="a9fc6-110">The media type of the **ITStream** interface must be audio for the **ITAudioDeviceControl** interface to be exposed.</span></span>

## <a name="members"></a><span data-ttu-id="a9fc6-111">Membri</span><span class="sxs-lookup"><span data-stu-id="a9fc6-111">Members</span></span>

<span data-ttu-id="a9fc6-112">L'interfaccia **ITAudioDeviceControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a9fc6-112">The **ITAudioDeviceControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a9fc6-113">**ITAudioDeviceControl** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a9fc6-113">**ITAudioDeviceControl** also has these types of members:</span></span>

-   [<span data-ttu-id="a9fc6-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="a9fc6-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9fc6-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="a9fc6-115">Methods</span></span>

<span data-ttu-id="a9fc6-116">L'interfaccia **ITAudioDeviceControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a9fc6-116">The **ITAudioDeviceControl** interface has these methods.</span></span>



| <span data-ttu-id="a9fc6-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="a9fc6-117">Method</span></span>                                              | <span data-ttu-id="a9fc6-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9fc6-118">Description</span></span>                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9fc6-119">**Ottieni**</span><span class="sxs-lookup"><span data-stu-id="a9fc6-119">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="a9fc6-120">Ottiene il valore di una [proprietà del dispositivo audio](audiodeviceproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="a9fc6-120">Gets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="a9fc6-121">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="a9fc6-121">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="a9fc6-122">Ottiene l'intervallo di valori validi per una determinata [proprietà del dispositivo audio](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc6-122">Gets the range of valid values for a given [audio device property](audiodeviceproperty.md).</span></span><br/> |
| [<span data-ttu-id="a9fc6-123">**Set**</span><span class="sxs-lookup"><span data-stu-id="a9fc6-123">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="a9fc6-124">Imposta il valore di una [proprietà del dispositivo audio](audiodeviceproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="a9fc6-124">Sets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="a9fc6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9fc6-125">Requirements</span></span>



| <span data-ttu-id="a9fc6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9fc6-126">Requirement</span></span> | <span data-ttu-id="a9fc6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a9fc6-127">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fc6-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a9fc6-128">TAPI version</span></span><br/> | <span data-ttu-id="a9fc6-129">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="a9fc6-129">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="a9fc6-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9fc6-130">Header</span></span><br/>       | <dl> <span data-ttu-id="a9fc6-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9fc6-131"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9fc6-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9fc6-132">Library</span></span><br/>      | <dl> <span data-ttu-id="a9fc6-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9fc6-133"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="a9fc6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a9fc6-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="a9fc6-135"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9fc6-135"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9fc6-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9fc6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fc6-137">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="a9fc6-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

