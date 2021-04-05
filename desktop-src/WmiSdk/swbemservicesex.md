---
description: Estende la funzionalità di SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Oggetto SWbemServicesEx (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130971"
---
# <a name="swbemservicesex-object"></a><span data-ttu-id="ae5ff-103">Oggetto SWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="ae5ff-103">SWbemServicesEx object</span></span>

<span data-ttu-id="ae5ff-104">L'oggetto **SWbemServicesEx** estende la funzionalità di [**SWbemServices**](swbemservices.md).</span><span class="sxs-lookup"><span data-stu-id="ae5ff-104">The **SWbemServicesEx** object extends the functionality of [**SWbemServices**](swbemservices.md).</span></span> <span data-ttu-id="ae5ff-105">I metodi [**put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) consentono il salvataggio di una classe o di un'istanza in più spazi dei nomi o in uno spazio dei nomi diverso da quello in cui è stata creata un'istanza.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-105">The [**Put**](swbemservicesex-put.md) and [**PutAsync**](swbemservicesex-putasync.md) methods allow a class or an instance to be saved to multiple namespaces or to a different namespace than the one where an instance was created.</span></span> <span data-ttu-id="ae5ff-106">Questo oggetto non può essere creato dalla chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-106">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="ae5ff-107">Membri</span><span class="sxs-lookup"><span data-stu-id="ae5ff-107">Members</span></span>

<span data-ttu-id="ae5ff-108">L'oggetto **SWbemServicesEx** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ae5ff-108">The **SWbemServicesEx** object has these types of members:</span></span>

-   [<span data-ttu-id="ae5ff-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ae5ff-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ae5ff-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ae5ff-110">Methods</span></span>

<span data-ttu-id="ae5ff-111">L'oggetto **SWbemServicesEx** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-111">The **SWbemServicesEx** object has these methods.</span></span>



| <span data-ttu-id="ae5ff-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="ae5ff-112">Method</span></span>                                       | <span data-ttu-id="ae5ff-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae5ff-113">Description</span></span>                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae5ff-114">**Mettere**</span><span class="sxs-lookup"><span data-stu-id="ae5ff-114">**Put**</span></span>](swbemservicesex-put.md)           | <span data-ttu-id="ae5ff-115">Salva l'oggetto nello spazio dei nomi associato all'oggetto **SWbemServicesEx** e restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che contiene il percorso dell'oggetto in cui sono stati scritti i dati.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-115">Saves the object to the namespace bound to the **SWbemServicesEx** object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span><br/> |
| [<span data-ttu-id="ae5ff-116">**PutAsync**</span><span class="sxs-lookup"><span data-stu-id="ae5ff-116">**PutAsync**</span></span>](swbemservicesex-putasync.md) | <span data-ttu-id="ae5ff-117">Salva un oggetto in modo asincrono in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-117">Saves an object asynchronously to a namespace.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ae5ff-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae5ff-118">Remarks</span></span>

<span data-ttu-id="ae5ff-119">I metodi di questa classe possono essere chiamati sia in modalità semisincrono che in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-119">The methods in this class can be called in either the semisynchronous mode or the asynchronous mode.</span></span> <span data-ttu-id="ae5ff-120">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ae5ff-120">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae5ff-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae5ff-121">Requirements</span></span>



| <span data-ttu-id="ae5ff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae5ff-122">Requirement</span></span> | <span data-ttu-id="ae5ff-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ae5ff-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5ff-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae5ff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ae5ff-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae5ff-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae5ff-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae5ff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ae5ff-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae5ff-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae5ff-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae5ff-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae5ff-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae5ff-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae5ff-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ae5ff-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae5ff-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ae5ff-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ae5ff-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ae5ff-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae5ff-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae5ff-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae5ff-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="ae5ff-134">CLSID</span></span><br/>                    | <span data-ttu-id="ae5ff-135">\_ISWBEMSERVICESEX CLSID</span><span class="sxs-lookup"><span data-stu-id="ae5ff-135">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="ae5ff-136">IID</span><span class="sxs-lookup"><span data-stu-id="ae5ff-136">IID</span></span><br/>                      | <span data-ttu-id="ae5ff-137">\_ISWBEMSERVICESEX IID</span><span class="sxs-lookup"><span data-stu-id="ae5ff-137">IID\_ISWbemServicesEx</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="ae5ff-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae5ff-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae5ff-139">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="ae5ff-139">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="ae5ff-140">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="ae5ff-140">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

