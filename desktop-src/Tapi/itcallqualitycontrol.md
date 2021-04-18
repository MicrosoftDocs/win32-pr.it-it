---
description: L'interfaccia ITCallQualityControl espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità della chiamata.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interfaccia ITCallQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328237"
---
# <a name="itcallqualitycontrol-interface"></a><span data-ttu-id="40d04-103">Interfaccia ITCallQualityControl</span><span class="sxs-lookup"><span data-stu-id="40d04-103">ITCallQualityControl interface</span></span>

<span data-ttu-id="40d04-104">\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="40d04-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="40d04-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="40d04-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="40d04-106">L'interfaccia **ITCallQualityControl** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità della chiamata.</span><span class="sxs-lookup"><span data-stu-id="40d04-106">The **ITCallQualityControl** interface exposes methods that allow an application to get and set parameters for call quality control.</span></span>

<span data-ttu-id="40d04-107">Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) e [H323 msp](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="40d04-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="40d04-108">Viene esposto solo quando una chiamata utilizza questi provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="40d04-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="40d04-109">Membri</span><span class="sxs-lookup"><span data-stu-id="40d04-109">Members</span></span>

<span data-ttu-id="40d04-110">L'interfaccia **ITCallQualityControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="40d04-110">The **ITCallQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="40d04-111">**ITCallQualityControl** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="40d04-111">**ITCallQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="40d04-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="40d04-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="40d04-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="40d04-113">Methods</span></span>

<span data-ttu-id="40d04-114">L'interfaccia **ITCallQualityControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="40d04-114">The **ITCallQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="40d04-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="40d04-115">Method</span></span>                                            | <span data-ttu-id="40d04-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40d04-116">Description</span></span>                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40d04-117">**Ottieni**</span><span class="sxs-lookup"><span data-stu-id="40d04-117">**Get**</span></span>](itcallqualitycontrol-get.md)           | <span data-ttu-id="40d04-118">Ottiene il valore di una [proprietà del controllo della qualità della chiamata](callqualityproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="40d04-118">Gets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="40d04-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="40d04-119">**GetRange**</span></span>](itcallqualitycontrol-getrange.md) | <span data-ttu-id="40d04-120">Ottiene l'intervallo di valori validi per una determinata [proprietà del controllo di qualità della chiamata](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="40d04-120">Gets the range of valid values for a given [call quality control property](callqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="40d04-121">**Set**</span><span class="sxs-lookup"><span data-stu-id="40d04-121">**Set**</span></span>](itcallqualitycontrol-set.md)           | <span data-ttu-id="40d04-122">Imposta il valore di una [proprietà del controllo della qualità della chiamata](callqualityproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="40d04-122">Sets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="40d04-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40d04-123">Requirements</span></span>



| <span data-ttu-id="40d04-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d04-124">Requirement</span></span> | <span data-ttu-id="40d04-125">Valore</span><span class="sxs-lookup"><span data-stu-id="40d04-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="40d04-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="40d04-126">TAPI version</span></span><br/> | <span data-ttu-id="40d04-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="40d04-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="40d04-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40d04-128">Header</span></span><br/>       | <dl> <span data-ttu-id="40d04-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="40d04-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="40d04-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="40d04-130">Library</span></span><br/>      | <dl> <span data-ttu-id="40d04-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40d04-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="40d04-132">DLL</span><span class="sxs-lookup"><span data-stu-id="40d04-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="40d04-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d04-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

