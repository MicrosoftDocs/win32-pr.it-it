---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Annulla la registrazione di una notifica registrata in precedenza per.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399516"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a><span data-ttu-id="2e094-103">Metodo IDXCoreAdapterFactory:: UnregisterEventNotification</span><span class="sxs-lookup"><span data-stu-id="2e094-103">IDXCoreAdapterFactory::UnregisterEventNotification method</span></span>

<span data-ttu-id="2e094-104">Annulla la registrazione di una notifica registrata in precedenza per.</span><span class="sxs-lookup"><span data-stu-id="2e094-104">Unregisters from a notification that you previously registered for.</span></span> <span data-ttu-id="2e094-105">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="2e094-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e094-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e094-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a><span data-ttu-id="2e094-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e094-107">Parameters</span></span>

### <a name="eventcookie"></a><span data-ttu-id="2e094-108">eventCookie</span><span class="sxs-lookup"><span data-stu-id="2e094-108">eventCookie</span></span>

<span data-ttu-id="2e094-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="2e094-109">Type: **uint32_t**</span></span>

<span data-ttu-id="2e094-110">Valore del cookie (restituito quando è stato chiamato [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) che rappresenta una registrazione precedente a cui si desidera annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="2e094-110">The cookie value (returned when you called [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) representing a prior registration that you now wish to unregister for.</span></span>

## <a name="returns"></a><span data-ttu-id="2e094-111">Restituisce</span><span class="sxs-lookup"><span data-stu-id="2e094-111">Returns</span></span>

<span data-ttu-id="2e094-112">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="2e094-112">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="2e094-113">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="2e094-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2e094-114">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2e094-114">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="2e094-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e094-115">Return value</span></span>|<span data-ttu-id="2e094-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e094-116">Description</span></span>|
|-|-|
|<span data-ttu-id="2e094-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2e094-117">E_INVALIDARG</span></span>|<span data-ttu-id="2e094-118">Il valore di *eventCookie* non è un cookie valido che rappresenta una registrazione precedente.</span><span class="sxs-lookup"><span data-stu-id="2e094-118">The value of *eventCookie* is not a valid cookie representing a prior registration.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2e094-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e094-119">Remarks</span></span>

<span data-ttu-id="2e094-120">**UnregisterEventNotification** restituisce solo dopo il completamento di tutti i callback in sospeso/in corso per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="2e094-120">**UnregisterEventNotification** returns only after all pending/in-progress callbacks for this registration have completed.</span></span> <span data-ttu-id="2e094-121">DXCore garantisce che non si verificheranno nuovi callback per questa registrazione dopo che è stato restituito **UnregisterEventNotification** .</span><span class="sxs-lookup"><span data-stu-id="2e094-121">DXCore guarantees that no new callbacks will occur for this registration after **UnregisterEventNotification** has returned.</span></span> <span data-ttu-id="2e094-122">Tuttavia, per evitare un deadlock, se si chiama **UnregisterEventNotification** dall'interno del callback, **UnregisterEventNotification** non attende il completamento del callback attivo.</span><span class="sxs-lookup"><span data-stu-id="2e094-122">However, to avoid a deadlock, if you call **UnregisterEventNotification** from within your callback, then **UnregisterEventNotification** doesn't wait for the active callback to complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e094-123">Prima di eliminare l'oggetto DXCore rappresentato dall'argomento *dxCoreObject* passato a [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), è necessario usare il valore del cookie per annullare la registrazione dell'oggetto dalle notifiche chiamando **UnregisterEventNotification**.</span><span class="sxs-lookup"><span data-stu-id="2e094-123">Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), you must use the cookie value to unregister that object from notifications by calling **UnregisterEventNotification**.</span></span> <span data-ttu-id="2e094-124">Se non si esegue questa operazione, viene generata un'eccezione irreversibile quando viene rilevata la situazione.</span><span class="sxs-lookup"><span data-stu-id="2e094-124">If you don't do that, then a fatal exception is raised when the situation is detected.</span></span>

<span data-ttu-id="2e094-125">Una volta annullata la registrazione di un valore di cookie, tale valore sarà quindi idoneo per essere restituito da una registrazione successiva</span><span class="sxs-lookup"><span data-stu-id="2e094-125">Once you unregister a cookie value, that value is then eligible for being returned by a subsequent registration</span></span>

## <a name="see-also"></a><span data-ttu-id="2e094-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e094-126">See also</span></span>

<span data-ttu-id="2e094-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="2e094-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>