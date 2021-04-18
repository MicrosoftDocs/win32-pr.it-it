---
description: L'interfaccia ITFormatControl espone metodi che consentono a un'applicazione di recuperare informazioni sul formato di un flusso di ricezione o trasmissione per una chiamata.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interfaccia ITFormatControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332005"
---
# <a name="itformatcontrol-interface"></a><span data-ttu-id="8bb51-103">Interfaccia ITFormatControl</span><span class="sxs-lookup"><span data-stu-id="8bb51-103">ITFormatControl interface</span></span>

<span data-ttu-id="8bb51-104">\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8bb51-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8bb51-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8bb51-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8bb51-106">L'interfaccia **ITFormatControl** espone metodi che consentono a un'applicazione di recuperare informazioni sul formato di un flusso di ricezione o trasmissione per una chiamata.</span><span class="sxs-lookup"><span data-stu-id="8bb51-106">The **ITFormatControl** interface exposes methods that allow an application to retrieve information concerning the format of a receive or transmit stream for a call.</span></span>

<span data-ttu-id="8bb51-107">Questa interfaccia viene implementata da [H323 msp](h323-msp.md) ed è esposta solo quando una chiamata utilizza questo provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="8bb51-107">This interface is implemented by the [H323 MSP](h323-msp.md) and is exposed only when a call uses this service provider.</span></span>

## <a name="members"></a><span data-ttu-id="8bb51-108">Membri</span><span class="sxs-lookup"><span data-stu-id="8bb51-108">Members</span></span>

<span data-ttu-id="8bb51-109">L'interfaccia **ITFormatControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8bb51-109">The **ITFormatControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8bb51-110">**ITFormatControl** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8bb51-110">**ITFormatControl** also has these types of members:</span></span>

-   [<span data-ttu-id="8bb51-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="8bb51-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8bb51-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="8bb51-112">Methods</span></span>

<span data-ttu-id="8bb51-113">L'interfaccia **ITFormatControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8bb51-113">The **ITFormatControl** interface has these methods.</span></span>



| <span data-ttu-id="8bb51-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="8bb51-114">Method</span></span>                                                                     | <span data-ttu-id="8bb51-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bb51-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="8bb51-116">**GetCurrentFormat**</span><span class="sxs-lookup"><span data-stu-id="8bb51-116">**GetCurrentFormat**</span></span>](itformatcontrol-getcurrentformat.md)               | <span data-ttu-id="8bb51-117">Ottiene il formato multimediale del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="8bb51-117">Gets the media format of the current stream.</span></span><br/>                        |
| [<span data-ttu-id="8bb51-118">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8bb51-118">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md) | <span data-ttu-id="8bb51-119">Ottiene il numero di funzionalità associate al formato corrente.</span><span class="sxs-lookup"><span data-stu-id="8bb51-119">Gets the number of capabilities associated with the current format.</span></span><br/> |
| [<span data-ttu-id="8bb51-120">**GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="8bb51-120">**GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)                     | <span data-ttu-id="8bb51-121">Ottiene le funzionalità associate a un indice di formato specificato.</span><span class="sxs-lookup"><span data-stu-id="8bb51-121">Gets the capabilities associated with a given format index.</span></span><br/>         |
| [<span data-ttu-id="8bb51-122">**ReleaseFormat**</span><span class="sxs-lookup"><span data-stu-id="8bb51-122">**ReleaseFormat**</span></span>](itformatcontrol-releaseformat.md)                     | <span data-ttu-id="8bb51-123">Rilascia la struttura associata al formato.</span><span class="sxs-lookup"><span data-stu-id="8bb51-123">Releases the structure associated with the format.</span></span><br/>                  |
| [<span data-ttu-id="8bb51-124">**ReOrderCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8bb51-124">**ReOrderCapabilities**</span></span>](itformatcontrol-reordercapabilities.md)         | <span data-ttu-id="8bb51-125">Imposta un nuovo ordine per le funzionalità di formattazione.</span><span class="sxs-lookup"><span data-stu-id="8bb51-125">Sets a new order for format capabilities.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="8bb51-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bb51-126">Requirements</span></span>



| <span data-ttu-id="8bb51-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb51-127">Requirement</span></span> | <span data-ttu-id="8bb51-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8bb51-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb51-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="8bb51-129">TAPI version</span></span><br/> | <span data-ttu-id="8bb51-130">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8bb51-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="8bb51-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bb51-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8bb51-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb51-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bb51-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="8bb51-133">Library</span></span><br/>      | <dl> <span data-ttu-id="8bb51-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bb51-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="8bb51-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8bb51-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="8bb51-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bb51-136"><dt>Tapi3.dll</dt></span></span> </dl> |



 

