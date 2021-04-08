---
title: IDXCoreAdapterList::GetAdapter
description: Recupera un adapter specifico in base all'indice da un oggetto elenco di adapter DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047171"
---
# <a name="idxcoreadapterlistgetadapter-method"></a><span data-ttu-id="16b95-103">Metodo IDXCoreAdapterList:: GetAdapter</span><span class="sxs-lookup"><span data-stu-id="16b95-103">IDXCoreAdapterList::GetAdapter method</span></span>

<span data-ttu-id="16b95-104">Recupera un adapter specifico in base all'indice da un oggetto elenco di adapter DXCore.</span><span class="sxs-lookup"><span data-stu-id="16b95-104">Retrieves a specific adapter by index from a DXCore adapter list object.</span></span> <span data-ttu-id="16b95-105">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="16b95-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="16b95-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16b95-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="16b95-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="16b95-107">Parameters</span></span>

### <a name="index"></a><span data-ttu-id="16b95-108">indice</span><span class="sxs-lookup"><span data-stu-id="16b95-108">index</span></span>

<span data-ttu-id="16b95-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="16b95-109">Type: **uint32_t**</span></span>

<span data-ttu-id="16b95-110">Indice in base zero, che identifica un'istanza dell'adapter all'interno dell'elenco di adapter DXCore.</span><span class="sxs-lookup"><span data-stu-id="16b95-110">A zero-based index, identifying an adapter instance within the DXCore adapter list.</span></span>

### <a name="riid"></a><span data-ttu-id="16b95-111">riid</span><span class="sxs-lookup"><span data-stu-id="16b95-111">riid</span></span>

<span data-ttu-id="16b95-112">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="16b95-112">Type: **REFIID**</span></span>

<span data-ttu-id="16b95-113">Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="16b95-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="16b95-114">Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="16b95-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="16b95-115">ppvAdapter [out]</span><span class="sxs-lookup"><span data-stu-id="16b95-115">ppvAdapter [out]</span></span>

<span data-ttu-id="16b95-116">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="16b95-116">Type: **void\*\***</span></span>

<span data-ttu-id="16b95-117">Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="16b95-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="16b95-118">In caso di esito positivo, *\* ppvAdapter* (l'indirizzo dereferenziato) contiene un puntatore alla scheda DXCore creata.</span><span class="sxs-lookup"><span data-stu-id="16b95-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="16b95-119">Restituisce</span><span class="sxs-lookup"><span data-stu-id="16b95-119">Returns</span></span>

<span data-ttu-id="16b95-120">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="16b95-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="16b95-121">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="16b95-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="16b95-122">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="16b95-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="16b95-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16b95-123">Return value</span></span>|<span data-ttu-id="16b95-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16b95-124">Description</span></span>|
|-|-|
|<span data-ttu-id="16b95-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="16b95-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="16b95-126">L' *Indice* è valido, ma lo stato dell'adapter non è più valido.</span><span class="sxs-lookup"><span data-stu-id="16b95-126">The *index* is valid, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="16b95-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="16b95-127">E_INVALIDARG</span></span>|<span data-ttu-id="16b95-128">L' *Indice* specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="16b95-128">The provided *index* is not valid.</span></span>|
|<span data-ttu-id="16b95-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="16b95-129">E_NOINTERFACE</span></span>|<span data-ttu-id="16b95-130">È stato specificato un valore non valido per *riid*.</span><span class="sxs-lookup"><span data-stu-id="16b95-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="16b95-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="16b95-131">E_POINTER</span></span>|<span data-ttu-id="16b95-132">`nullptr` fornito per *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="16b95-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="16b95-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="16b95-133">Remarks</span></span>

<span data-ttu-id="16b95-134">Più chiamate che passano un indice che rappresenta lo stesso adapter restituiscono puntatori di interfaccia identici, anche in diversi elenchi di adapter.</span><span class="sxs-lookup"><span data-stu-id="16b95-134">Multiple calls passing an index that represents the same adapter return identical interface pointers, even across different adapter lists.</span></span> <span data-ttu-id="16b95-135">Di conseguenza, è possibile confrontare i puntatori all'interfaccia per determinare se più puntatori fanno riferimento allo stesso oggetto adapter.</span><span class="sxs-lookup"><span data-stu-id="16b95-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="16b95-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16b95-136">See also</span></span>

<span data-ttu-id="16b95-137">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="16b95-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>