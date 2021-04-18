---
description: L'interfaccia ITAudioSettings espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interfaccia ITAudioSettings (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331598"
---
# <a name="itaudiosettings-interface"></a><span data-ttu-id="f5ffe-103">Interfaccia ITAudioSettings</span><span class="sxs-lookup"><span data-stu-id="f5ffe-103">ITAudioSettings interface</span></span>

<span data-ttu-id="f5ffe-104">\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f5ffe-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f5ffe-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f5ffe-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f5ffe-106">L'interfaccia **ITAudioSettings** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="f5ffe-106">The **ITAudioSettings** interface exposes methods that allow an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="f5ffe-107">Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) e [H323 msp](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="f5ffe-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="f5ffe-108">Viene esposto solo quando una chiamata utilizza questi provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="f5ffe-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="f5ffe-109">Membri</span><span class="sxs-lookup"><span data-stu-id="f5ffe-109">Members</span></span>

<span data-ttu-id="f5ffe-110">L'interfaccia **ITAudioSettings** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f5ffe-110">The **ITAudioSettings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f5ffe-111">**ITAudioSettings** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f5ffe-111">**ITAudioSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="f5ffe-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="f5ffe-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f5ffe-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f5ffe-113">Methods</span></span>

<span data-ttu-id="f5ffe-114">L'interfaccia **ITAudioSettings** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f5ffe-114">The **ITAudioSettings** interface has these methods.</span></span>



| <span data-ttu-id="f5ffe-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="f5ffe-115">Method</span></span>                                              | <span data-ttu-id="f5ffe-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5ffe-116">Description</span></span>                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5ffe-117">**Ottieni**</span><span class="sxs-lookup"><span data-stu-id="f5ffe-117">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="f5ffe-118">Ottiene il valore di una [proprietà dell'impostazione audio](audiosettingsproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="f5ffe-118">Gets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="f5ffe-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="f5ffe-119">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="f5ffe-120">Ottiene l'intervallo di valori validi per una [proprietà di impostazione audio](audiosettingsproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="f5ffe-120">Gets the range of valid values for a given [audio setting property](audiosettingsproperty.md).</span></span><br/> |
| [<span data-ttu-id="f5ffe-121">**Set**</span><span class="sxs-lookup"><span data-stu-id="f5ffe-121">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="f5ffe-122">Imposta il valore di una [proprietà dell'impostazione audio](audiosettingsproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="f5ffe-122">Sets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="f5ffe-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5ffe-123">Requirements</span></span>



| <span data-ttu-id="f5ffe-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ffe-124">Requirement</span></span> | <span data-ttu-id="f5ffe-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ffe-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ffe-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f5ffe-126">TAPI version</span></span><br/> | <span data-ttu-id="f5ffe-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f5ffe-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="f5ffe-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5ffe-128">Header</span></span><br/>       | <dl> <span data-ttu-id="f5ffe-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ffe-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5ffe-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5ffe-130">Library</span></span><br/>      | <dl> <span data-ttu-id="f5ffe-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5ffe-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="f5ffe-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f5ffe-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="f5ffe-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5ffe-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

