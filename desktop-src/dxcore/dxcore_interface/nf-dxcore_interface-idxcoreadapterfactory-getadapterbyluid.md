---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Recupera l'oggetto adattatore DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) per un LUID specificato, se disponibile.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399450"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a><span data-ttu-id="04d60-103">Metodo IDXCoreAdapterFactory:: GetAdapterByLuid</span><span class="sxs-lookup"><span data-stu-id="04d60-103">IDXCoreAdapterFactory::GetAdapterByLuid method</span></span>

<span data-ttu-id="04d60-104">Recupera l'oggetto adattatore DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) per un LUID specificato, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="04d60-104">Retrieves the DXCore adapter object ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) for a specified LUID, if available.</span></span> <span data-ttu-id="04d60-105">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="04d60-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="04d60-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04d60-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="04d60-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="04d60-107">Parameters</span></span>

### <a name="adapterluid"></a><span data-ttu-id="04d60-108">adapterLUID</span><span class="sxs-lookup"><span data-stu-id="04d60-108">adapterLUID</span></span>

<span data-ttu-id="04d60-109">Tipo: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span><span class="sxs-lookup"><span data-stu-id="04d60-109">Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span></span>

<span data-ttu-id="04d60-110">Valore univoco locale che identifica l'istanza dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="04d60-110">The locally unique value that identifies the adapter instance.</span></span>

### <a name="riid-in"></a><span data-ttu-id="04d60-111">riid [in]</span><span class="sxs-lookup"><span data-stu-id="04d60-111">riid [in]</span></span>

<span data-ttu-id="04d60-112">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="04d60-112">Type: **REFIID**</span></span>

<span data-ttu-id="04d60-113">Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="04d60-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="04d60-114">Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="04d60-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="04d60-115">ppvAdapter [out]</span><span class="sxs-lookup"><span data-stu-id="04d60-115">ppvAdapter [out]</span></span>

<span data-ttu-id="04d60-116">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="04d60-116">Type: **void\*\***</span></span>

<span data-ttu-id="04d60-117">Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="04d60-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="04d60-118">In caso di esito positivo, *\* ppvAdapter* (l'indirizzo dereferenziato) contiene un puntatore alla scheda DXCore creata.</span><span class="sxs-lookup"><span data-stu-id="04d60-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="04d60-119">Restituisce</span><span class="sxs-lookup"><span data-stu-id="04d60-119">Returns</span></span>

<span data-ttu-id="04d60-120">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="04d60-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="04d60-121">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="04d60-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="04d60-122">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="04d60-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="04d60-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04d60-123">Return value</span></span>|<span data-ttu-id="04d60-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04d60-124">Description</span></span>|
|-|-|
|<span data-ttu-id="04d60-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="04d60-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="04d60-126">L'adapter LUID passato in *adapterLUID* è riconosciuto, ma lo stato dell'adapter non è più valido.</span><span class="sxs-lookup"><span data-stu-id="04d60-126">The adapter LUID passed in *adapterLUID* is recognized, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="04d60-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="04d60-127">E_INVALIDARG</span></span>|<span data-ttu-id="04d60-128">Nessun adapter di questo tipo LUID come il valore passato in *adapterLUID* è disponibile tramite dxcore.</span><span class="sxs-lookup"><span data-stu-id="04d60-128">No such adapter LUID as the value passed in *adapterLUID* is available through DXCore.</span></span>|
|<span data-ttu-id="04d60-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="04d60-129">E_NOINTERFACE</span></span>|<span data-ttu-id="04d60-130">È stato specificato un valore non valido per *riid*.</span><span class="sxs-lookup"><span data-stu-id="04d60-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="04d60-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="04d60-131">E_POINTER</span></span>|<span data-ttu-id="04d60-132">`nullptr` fornito per *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="04d60-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="04d60-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="04d60-133">Remarks</span></span>

<span data-ttu-id="04d60-134">Più chiamate che passano lo stesso [LUID](/windows/win32/api/winnt/ns-winnt-luid) restituiscono puntatori di interfaccia identici.</span><span class="sxs-lookup"><span data-stu-id="04d60-134">Multiple calls passing the same [LUID](/windows/win32/api/winnt/ns-winnt-luid) return identical interface pointers.</span></span> <span data-ttu-id="04d60-135">Di conseguenza, è possibile confrontare i puntatori all'interfaccia per determinare se più puntatori fanno riferimento allo stesso oggetto adapter.</span><span class="sxs-lookup"><span data-stu-id="04d60-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="04d60-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04d60-136">See also</span></span>

<span data-ttu-id="04d60-137">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="04d60-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>