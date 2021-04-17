---
title: IDXCoreAdapter::SetState
description: Imposta lo stato dell'elemento specificato nell'adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300214"
---
# <a name="idxcoreadaptersetstate-method"></a><span data-ttu-id="f0492-103">Metodo IDXCoreAdapter:: sestate</span><span class="sxs-lookup"><span data-stu-id="f0492-103">IDXCoreAdapter::SetState method</span></span>

<span data-ttu-id="f0492-104">Imposta lo stato dell'elemento specificato nell'adapter.</span><span class="sxs-lookup"><span data-stu-id="f0492-104">Sets the state of the specified item on the adapter.</span></span> <span data-ttu-id="f0492-105">Prima di chiamare **lo stato** per un tipo di proprietà, chiamare [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) per verificare che l'impostazione del tipo di stato sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f0492-105">Before calling **SetState** for a property type, call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0492-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0492-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a><span data-ttu-id="f0492-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0492-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="f0492-108">state</span><span class="sxs-lookup"><span data-stu-id="f0492-108">state</span></span>

<span data-ttu-id="f0492-109">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="f0492-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="f0492-110">Tipo di elemento di stato nell'adapter di cui si desidera impostare lo stato.</span><span class="sxs-lookup"><span data-stu-id="f0492-110">The kind of state item on the adapter whose state you wish to set.</span></span> <span data-ttu-id="f0492-111">Per ulteriori informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f0492-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="f0492-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="f0492-112">inputStateDetailsSize</span></span>

<span data-ttu-id="f0492-113">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="f0492-113">Type: **size_t**</span></span>

<span data-ttu-id="f0492-114">Dimensioni, in byte, del buffer dei dettagli sullo stato di input che è possibile allocare e fornire in *inputStateDetails*.</span><span class="sxs-lookup"><span data-stu-id="f0492-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="f0492-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="f0492-115">inputStateDetails [in]</span></span>

<span data-ttu-id="f0492-116">Tipo: **void const \***</span><span class="sxs-lookup"><span data-stu-id="f0492-116">Type: **void const\***</span></span>

<span data-ttu-id="f0492-117">Puntatore facoltativo a un buffer di dettagli dello stato di input costante allocato nell'applicazione, contenente tutte le informazioni sulla richiesta richieste per il tipo di stato specificato in *stato*.</span><span class="sxs-lookup"><span data-stu-id="f0492-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="f0492-118">Per ulteriori informazioni su qualsiasi requisito del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f0492-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="inputdatasize"></a><span data-ttu-id="f0492-119">inputDataSize</span><span class="sxs-lookup"><span data-stu-id="f0492-119">inputDataSize</span></span>

<span data-ttu-id="f0492-120">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="f0492-120">Type: **size_t**</span></span>

<span data-ttu-id="f0492-121">Dimensione, in byte, del buffer di input allocato e fornito in *inputData*.</span><span class="sxs-lookup"><span data-stu-id="f0492-121">The size, in bytes, of the input buffer that you allocate and provide in *inputData*.</span></span>

### <a name="inputdata-in"></a><span data-ttu-id="f0492-122">inputData [in]</span><span class="sxs-lookup"><span data-stu-id="f0492-122">inputData [in]</span></span>

<span data-ttu-id="f0492-123">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="f0492-123">Type: **void\***</span></span>

<span data-ttu-id="f0492-124">Puntatore a un buffer di input allocato nell'applicazione, che contiene le informazioni sullo stato da impostare per l'elemento di stato il cui tipo è *stato* specificato nello stato.</span><span class="sxs-lookup"><span data-stu-id="f0492-124">A pointer to an input buffer that you allocate in your application, containing the state information to set for the state item whose kind you specify in *state*.</span></span> <span data-ttu-id="f0492-125">Per ulteriori informazioni sul requisito del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f0492-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the input buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="f0492-126">Restituisce</span><span class="sxs-lookup"><span data-stu-id="f0492-126">Returns</span></span>

<span data-ttu-id="f0492-127">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f0492-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f0492-128">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f0492-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f0492-129">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f0492-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="f0492-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0492-130">Return value</span></span>|<span data-ttu-id="f0492-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0492-131">Description</span></span>|
|-|-|
|<span data-ttu-id="f0492-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="f0492-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="f0492-133">Lo stato dell'adapter non è più valido.</span><span class="sxs-lookup"><span data-stu-id="f0492-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="f0492-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="f0492-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="f0492-135">Il tipo di stato specificato nello *stato* non è riconosciuto dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f0492-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="f0492-136">Chiamare [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) per verificare che l'impostazione del tipo di stato sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f0492-136">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="f0492-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="f0492-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="f0492-138">Il tipo di stato specificato in *state* non è supportato dall'adapter.</span><span class="sxs-lookup"><span data-stu-id="f0492-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="f0492-139">Chiamare [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) per verificare che l'impostazione del tipo di stato sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f0492-139">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="f0492-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f0492-140">E_INVALIDARG</span></span>|<span data-ttu-id="f0492-141">Viene fornita una dimensione del buffer insufficiente per *inputData* (o per *inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).</span><span class="sxs-lookup"><span data-stu-id="f0492-141">An insufficient buffer size is provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="f0492-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="f0492-142">E_POINTER</span></span>|<span data-ttu-id="f0492-143">`nullptr` è stato specificato per *inputData* (o per *inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).</span><span class="sxs-lookup"><span data-stu-id="f0492-143">`nullptr` was provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="see-also"></a><span data-ttu-id="f0492-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0492-144">See also</span></span>

<span data-ttu-id="f0492-145">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f0492-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>