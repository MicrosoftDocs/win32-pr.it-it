---
title: IDXCoreAdapter::QueryState
description: Recupera lo stato corrente dell'elemento specificato nell'adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300215"
---
# <a name="idxcoreadapterquerystate-method"></a><span data-ttu-id="63144-103">Metodo IDXCoreAdapter:: QueryState</span><span class="sxs-lookup"><span data-stu-id="63144-103">IDXCoreAdapter::QueryState method</span></span>

<span data-ttu-id="63144-104">Recupera lo stato corrente dell'elemento specificato nell'adapter.</span><span class="sxs-lookup"><span data-stu-id="63144-104">Retrieves the current state of the specified item on the adapter.</span></span> <span data-ttu-id="63144-105">Prima di chiamare **QueryState** per un tipo di proprietà, chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di una query sul tipo di stato sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63144-105">Before calling **QueryState** for a property type, call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="63144-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63144-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a><span data-ttu-id="63144-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="63144-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="63144-108">state</span><span class="sxs-lookup"><span data-stu-id="63144-108">state</span></span>

<span data-ttu-id="63144-109">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="63144-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="63144-110">Tipo di elemento di stato nell'adapter di cui si desidera recuperare lo stato.</span><span class="sxs-lookup"><span data-stu-id="63144-110">The kind of state item on the adapter whose state you wish to retrieve.</span></span> <span data-ttu-id="63144-111">Per ulteriori informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="63144-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="63144-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="63144-112">inputStateDetailsSize</span></span>

<span data-ttu-id="63144-113">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="63144-113">Type: **size_t**</span></span>

<span data-ttu-id="63144-114">Dimensioni, in byte, del buffer dei dettagli sullo stato di input che è possibile allocare e fornire in *inputStateDetails*.</span><span class="sxs-lookup"><span data-stu-id="63144-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="63144-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="63144-115">inputStateDetails [in]</span></span>

<span data-ttu-id="63144-116">Tipo: **void const \***</span><span class="sxs-lookup"><span data-stu-id="63144-116">Type: **void const\***</span></span>

<span data-ttu-id="63144-117">Puntatore facoltativo a un buffer di dettagli dello stato di input costante allocato nell'applicazione, contenente tutte le informazioni sulla richiesta richieste per il tipo di stato specificato in *stato*.</span><span class="sxs-lookup"><span data-stu-id="63144-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="63144-118">Per ulteriori informazioni su qualsiasi requisito del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="63144-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="outputbuffersize"></a><span data-ttu-id="63144-119">outputBufferSize</span><span class="sxs-lookup"><span data-stu-id="63144-119">outputBufferSize</span></span>

<span data-ttu-id="63144-120">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="63144-120">Type: **size_t**</span></span>

<span data-ttu-id="63144-121">Dimensione, in byte, del buffer di output allocato e fornito in *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="63144-121">The size, in bytes, of the output buffer that you allocate and provide in *outputBuffer*.</span></span>

### <a name="outputbuffer-out"></a><span data-ttu-id="63144-122">outputBuffer [out]</span><span class="sxs-lookup"><span data-stu-id="63144-122">outputBuffer [out]</span></span>

<span data-ttu-id="63144-123">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="63144-123">Type: **void\***</span></span>

<span data-ttu-id="63144-124">Puntatore a un buffer di output allocato nell'applicazione e che la funzione compila.</span><span class="sxs-lookup"><span data-stu-id="63144-124">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="63144-125">Per altre informazioni sul requisito del buffer di output per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="63144-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the output buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="63144-126">Restituisce</span><span class="sxs-lookup"><span data-stu-id="63144-126">Returns</span></span>

<span data-ttu-id="63144-127">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="63144-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="63144-128">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="63144-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="63144-129">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="63144-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="63144-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63144-130">Return value</span></span>|<span data-ttu-id="63144-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63144-131">Description</span></span>|
|-|-|
|<span data-ttu-id="63144-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="63144-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="63144-133">Lo stato dell'adapter non è più valido.</span><span class="sxs-lookup"><span data-stu-id="63144-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="63144-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="63144-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="63144-135">Il tipo di stato specificato nello *stato* non è riconosciuto dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63144-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="63144-136">Chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di una query sul tipo di stato sia disponibile per questo adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63144-136">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="63144-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="63144-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="63144-138">Il tipo di stato specificato in *state* non è supportato dall'adapter.</span><span class="sxs-lookup"><span data-stu-id="63144-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="63144-139">Chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di una query sul tipo di stato sia disponibile per questo adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63144-139">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="63144-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="63144-140">E_INVALIDARG</span></span>|<span data-ttu-id="63144-141">Viene fornita una dimensione del buffer insufficiente per *outputBuffer* (o per *inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).</span><span class="sxs-lookup"><span data-stu-id="63144-141">An insufficient buffer size is provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="63144-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="63144-142">E_POINTER</span></span>|<span data-ttu-id="63144-143">`nullptr` è stato specificato per *outputBuffer* (o per *inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).</span><span class="sxs-lookup"><span data-stu-id="63144-143">`nullptr` was provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="remarks"></a><span data-ttu-id="63144-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="63144-144">Remarks</span></span>

<span data-ttu-id="63144-145">Vedere [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) per altre informazioni su ogni tipo di stato dell'adapter e sugli input e sugli output usati.</span><span class="sxs-lookup"><span data-stu-id="63144-145">See [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind, and what inputs and outputs are used.</span></span> <span data-ttu-id="63144-146">Questa funzione azzera il buffer *outputBuffer* prima di riempirlo.</span><span class="sxs-lookup"><span data-stu-id="63144-146">This function zeros out the *outputBuffer* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="63144-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63144-147">See also</span></span>

<span data-ttu-id="63144-148">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="63144-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>