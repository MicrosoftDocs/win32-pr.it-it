---
description: ITStreamQualityControl espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità del flusso.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interfaccia ITStreamQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329324"
---
# <a name="itstreamqualitycontrol-interface"></a><span data-ttu-id="32490-103">Interfaccia ITStreamQualityControl</span><span class="sxs-lookup"><span data-stu-id="32490-103">ITStreamQualityControl interface</span></span>

<span data-ttu-id="32490-104">\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="32490-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="32490-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="32490-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="32490-106">**ITStreamQualityControl** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità del flusso.</span><span class="sxs-lookup"><span data-stu-id="32490-106">The **ITStreamQualityControl** exposes methods that allow an application to get and set parameters for stream quality control.</span></span>

<span data-ttu-id="32490-107">Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) e [H323 msp](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="32490-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="32490-108">Viene esposto solo quando una chiamata utilizza questi provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="32490-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="32490-109">Membri</span><span class="sxs-lookup"><span data-stu-id="32490-109">Members</span></span>

<span data-ttu-id="32490-110">L'interfaccia **ITStreamQualityControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="32490-110">The **ITStreamQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="32490-111">**ITStreamQualityControl** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="32490-111">**ITStreamQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="32490-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="32490-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="32490-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="32490-113">Methods</span></span>

<span data-ttu-id="32490-114">L'interfaccia **ITStreamQualityControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="32490-114">The **ITStreamQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="32490-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="32490-115">Method</span></span>                                              | <span data-ttu-id="32490-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32490-116">Description</span></span>                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32490-117">**Ottieni**</span><span class="sxs-lookup"><span data-stu-id="32490-117">**Get**</span></span>](itstreamqualitycontrol-get.md)           | <span data-ttu-id="32490-118">Ottiene il valore di una [proprietà di qualità del flusso](streamqualityproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="32490-118">Gets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="32490-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="32490-119">**GetRange**</span></span>](itstreamqualitycontrol-getrange.md) | <span data-ttu-id="32490-120">Ottiene l'intervallo di valori validi per una determinata [proprietà di qualità del flusso](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="32490-120">Gets the range of valid values for a given [stream quality property](streamqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="32490-121">**Set**</span><span class="sxs-lookup"><span data-stu-id="32490-121">**Set**</span></span>](itstreamqualitycontrol-set.md)           | <span data-ttu-id="32490-122">Imposta il valore di una [proprietà di qualità del flusso](streamqualityproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="32490-122">Sets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="32490-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32490-123">Requirements</span></span>



| <span data-ttu-id="32490-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="32490-124">Requirement</span></span> | <span data-ttu-id="32490-125">Valore</span><span class="sxs-lookup"><span data-stu-id="32490-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="32490-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="32490-126">TAPI version</span></span><br/> | <span data-ttu-id="32490-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="32490-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="32490-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32490-128">Header</span></span><br/>       | <dl> <span data-ttu-id="32490-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="32490-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="32490-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="32490-130">Library</span></span><br/>      | <dl> <span data-ttu-id="32490-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32490-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="32490-132">DLL</span><span class="sxs-lookup"><span data-stu-id="32490-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="32490-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32490-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

