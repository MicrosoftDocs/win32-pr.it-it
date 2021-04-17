---
title: IDXCoreAdapter::GetPropertySize
description: Per una proprietà dell'adapter specificata, recupera la dimensione del buffer, in byte, necessaria per una chiamata a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299974"
---
# <a name="idxcoreadaptergetpropertysize-method"></a><span data-ttu-id="dbe46-103">Metodo IDXCoreAdapter:: GetPropertySize</span><span class="sxs-lookup"><span data-stu-id="dbe46-103">IDXCoreAdapter::GetPropertySize method</span></span>

<span data-ttu-id="dbe46-104">Per una proprietà dell'adapter specificata, recupera la dimensione del buffer, in byte, necessaria per una chiamata a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="dbe46-104">For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span> <span data-ttu-id="dbe46-105">Prima di chiamare **GetPropertySize** per un tipo di proprietà, chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbe46-105">Before calling **GetPropertySize** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe46-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbe46-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a><span data-ttu-id="dbe46-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbe46-107">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="dbe46-108">proprietà</span><span class="sxs-lookup"><span data-stu-id="dbe46-108">property</span></span>

<span data-ttu-id="dbe46-109">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="dbe46-109">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="dbe46-110">Tipo della proprietà le cui dimensioni, in byte, si desidera recuperare.</span><span class="sxs-lookup"><span data-stu-id="dbe46-110">The type of the property whose size, in bytes, you wish to retrieve.</span></span>

### <a name="buffersize-out"></a><span data-ttu-id="dbe46-111">bufferSize [out]</span><span class="sxs-lookup"><span data-stu-id="dbe46-111">bufferSize [out]</span></span>

<span data-ttu-id="dbe46-112">Tipo: **size_t \***</span><span class="sxs-lookup"><span data-stu-id="dbe46-112">Type: **size_t\***</span></span>

<span data-ttu-id="dbe46-113">Puntatore a un valore **size_t** .</span><span class="sxs-lookup"><span data-stu-id="dbe46-113">A pointer to a **size_t** value.</span></span> <span data-ttu-id="dbe46-114">La funzione dereferenzia il puntatore e imposta il valore sulla dimensione, in byte, del buffer di output che è necessario allocare e passare come argomento *PropertyData* nella chiamata a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="dbe46-114">The function dereferences the pointer and sets the value to the size, in bytes, of the output buffer that you should allocate and pass as the *propertyData* argument in your call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

## <a name="returns"></a><span data-ttu-id="dbe46-115">Restituisce</span><span class="sxs-lookup"><span data-stu-id="dbe46-115">Returns</span></span>

<span data-ttu-id="dbe46-116">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="dbe46-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="dbe46-117">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe46-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="dbe46-118">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="dbe46-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="dbe46-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbe46-119">Return value</span></span>|<span data-ttu-id="dbe46-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbe46-120">Description</span></span>|
|-|-|
|<span data-ttu-id="dbe46-121">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="dbe46-121">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="dbe46-122">Il tipo di proprietà specificato nella *Proprietà* non è riconosciuto dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbe46-122">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="dbe46-123">Chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbe46-123">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="dbe46-124">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="dbe46-124">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="dbe46-125">Il tipo di proprietà specificato nella *Proprietà* non è supportato dall'adapter.</span><span class="sxs-lookup"><span data-stu-id="dbe46-125">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="dbe46-126">Chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbe46-126">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="dbe46-127">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="dbe46-127">E_POINTER</span></span>|<span data-ttu-id="dbe46-128">`nullptr` fornito per *bufferSize*.</span><span class="sxs-lookup"><span data-stu-id="dbe46-128">`nullptr` was provided for *bufferSize*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dbe46-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbe46-129">Remarks</span></span>

<span data-ttu-id="dbe46-130">È possibile chiamare **GetPropertySize** su un adapter non più valido &mdash; . la funzione non avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="dbe46-130">You can call **GetPropertySize** on an adapter that's no longer valid&mdash;the function won't fail.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbe46-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbe46-131">See also</span></span>

<span data-ttu-id="dbe46-132">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="dbe46-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>