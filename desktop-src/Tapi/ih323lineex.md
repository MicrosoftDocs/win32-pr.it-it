---
description: L'interfaccia IH323LineEx viene implementata da H323 MSP ed è disponibile solo per gli oggetti Address H. 323. Questa interfaccia espone i metodi che consentono la creazione e la manipolazione di terminali che possono comunicare tra client H323 e SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interfaccia IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329951"
---
# <a name="ih323lineex-interface"></a><span data-ttu-id="825c6-104">Interfaccia IH323LineEx</span><span class="sxs-lookup"><span data-stu-id="825c6-104">IH323LineEx interface</span></span>

<span data-ttu-id="825c6-105">\[**IH323LineEx** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="825c6-105">\[**IH323LineEx** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="825c6-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="825c6-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="825c6-107">L'interfaccia **IH323LineEx** viene implementata da [H323 msp](h323-msp.md) ed è disponibile solo per gli oggetti Address H. 323.</span><span class="sxs-lookup"><span data-stu-id="825c6-107">The **IH323LineEx** interface is implemented by the [H323 MSP](h323-msp.md) and is available only on H.323 address objects.</span></span> <span data-ttu-id="825c6-108">Questa interfaccia espone i metodi che consentono la creazione e la manipolazione di terminali che possono comunicare tra client H323 e SDP.</span><span class="sxs-lookup"><span data-stu-id="825c6-108">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span>

> [!Note]  
> <span data-ttu-id="825c6-109">Tutti i metodi in questa interfaccia devono essere chiamati solo dopo la registrazione per le chiamate in ingresso su questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="825c6-109">All methods in this interface should be called only after registering for incoming calls on this address.</span></span>

 

## <a name="members"></a><span data-ttu-id="825c6-110">Membri</span><span class="sxs-lookup"><span data-stu-id="825c6-110">Members</span></span>

<span data-ttu-id="825c6-111">L'interfaccia **IH323LineEx** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="825c6-111">The **IH323LineEx** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="825c6-112">**IH323LineEx** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="825c6-112">**IH323LineEx** also has these types of members:</span></span>

-   [<span data-ttu-id="825c6-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="825c6-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="825c6-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="825c6-114">Methods</span></span>

<span data-ttu-id="825c6-115">L'interfaccia **IH323LineEx** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="825c6-115">The **IH323LineEx** interface has these methods.</span></span>



| <span data-ttu-id="825c6-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="825c6-116">Method</span></span>                                                                                 | <span data-ttu-id="825c6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="825c6-117">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="825c6-118">**Alias**</span><span class="sxs-lookup"><span data-stu-id="825c6-118">**SetAlias**</span></span>](ih323lineex-setalias.md)                                               | <span data-ttu-id="825c6-119">Configura un alias H. 323 predefinito per l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="825c6-119">Configures a default H.323 alias for the address.</span></span><br/>             |
| [<span data-ttu-id="825c6-120">**SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="825c6-120">**SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md) | <span data-ttu-id="825c6-121">Configura la ponderazione delle preferenze per le funzionalità predefinite.</span><span class="sxs-lookup"><span data-stu-id="825c6-121">Configures the preference weighting for default capabilities.</span></span><br/> |
| [<span data-ttu-id="825c6-122">**SetExternalT120Address**</span><span class="sxs-lookup"><span data-stu-id="825c6-122">**SetExternalT120Address**</span></span>](ih323lineex-setexternalt120address.md)                   | <span data-ttu-id="825c6-123">Configura un indirizzo T. 120 esterno per lo scambio di dati.</span><span class="sxs-lookup"><span data-stu-id="825c6-123">Configures an external T.120 address for data exchange.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="825c6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="825c6-124">Requirements</span></span>



| <span data-ttu-id="825c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="825c6-125">Requirement</span></span> | <span data-ttu-id="825c6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="825c6-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="825c6-127">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="825c6-127">TAPI version</span></span><br/> | <span data-ttu-id="825c6-128">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="825c6-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="825c6-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="825c6-129">Header</span></span><br/>       | <dl> <span data-ttu-id="825c6-130"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="825c6-130"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="825c6-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="825c6-131">Library</span></span><br/>      | <dl> <span data-ttu-id="825c6-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="825c6-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="825c6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="825c6-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="825c6-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="825c6-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="825c6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="825c6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825c6-136">MSP H323</span><span class="sxs-lookup"><span data-stu-id="825c6-136">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

