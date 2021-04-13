---
title: IDXCoreAdapter::GetProperty
description: Recupera il valore della proprietà dell'adapter specificata.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338975"
---
# <a name="idxcoreadaptergetproperty-method"></a><span data-ttu-id="adae7-103">Metodo IDXCoreAdapter:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="adae7-103">IDXCoreAdapter::GetProperty method</span></span>

<span data-ttu-id="adae7-104">Recupera il valore della proprietà dell'adapter specificata.</span><span class="sxs-lookup"><span data-stu-id="adae7-104">Retrieves the value of the specified adapter property.</span></span> <span data-ttu-id="adae7-105">Prima di chiamare **GetProperty** per un tipo di proprietà, chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="adae7-105">Before calling **GetProperty** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span> <span data-ttu-id="adae7-106">Inoltre, prima di chiamare **GetProperty**, chiamare [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per determinare la dimensione necessaria del buffer in cui ricevere il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="adae7-106">Also before calling **GetProperty**, call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the necessary size of the buffer in which to receive the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="adae7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="adae7-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a><span data-ttu-id="adae7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="adae7-108">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="adae7-109">proprietà</span><span class="sxs-lookup"><span data-stu-id="adae7-109">property</span></span>

<span data-ttu-id="adae7-110">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="adae7-110">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="adae7-111">Tipo della proprietà di cui si desidera recuperare il valore.</span><span class="sxs-lookup"><span data-stu-id="adae7-111">The type of the property whose value you wish to retrieve.</span></span> <span data-ttu-id="adae7-112">Per ulteriori informazioni su ogni proprietà dell'adapter, vedere la tabella in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="adae7-112">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

### <a name="buffersize"></a><span data-ttu-id="adae7-113">bufferSize</span><span class="sxs-lookup"><span data-stu-id="adae7-113">bufferSize</span></span>

<span data-ttu-id="adae7-114">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="adae7-114">Type: **size_t**</span></span>

<span data-ttu-id="adae7-115">Dimensione, in byte, del buffer di output allocato e fornito in *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="adae7-115">The size, in bytes, of the output buffer that you allocate and provide in *propertyData*.</span></span>

### <a name="propertydata-out"></a><span data-ttu-id="adae7-116">propertyData [out]</span><span class="sxs-lookup"><span data-stu-id="adae7-116">propertyData [out]</span></span>

<span data-ttu-id="adae7-117">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="adae7-117">Type: **void\***</span></span>

<span data-ttu-id="adae7-118">Puntatore a un buffer di output allocato nell'applicazione e che la funzione compila.</span><span class="sxs-lookup"><span data-stu-id="adae7-118">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="adae7-119">Chiamare [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per determinare le dimensioni del buffer *PropertyData* per una determinata proprietà dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="adae7-119">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="adae7-120">Restituisce</span><span class="sxs-lookup"><span data-stu-id="adae7-120">Returns</span></span>

<span data-ttu-id="adae7-121">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="adae7-121">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="adae7-122">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="adae7-122">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="adae7-123">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="adae7-123">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="adae7-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="adae7-124">Return value</span></span>|<span data-ttu-id="adae7-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adae7-125">Description</span></span>|
|-|-|
|<span data-ttu-id="adae7-126">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="adae7-126">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="adae7-127">Il tipo di proprietà specificato nella *Proprietà* non è riconosciuto dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="adae7-127">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="adae7-128">Chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="adae7-128">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="adae7-129">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="adae7-129">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="adae7-130">Il tipo di proprietà specificato nella *Proprietà* non è supportato dall'adapter.</span><span class="sxs-lookup"><span data-stu-id="adae7-130">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="adae7-131">Chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="adae7-131">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="adae7-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="adae7-132">E_INVALIDARG</span></span>|<span data-ttu-id="adae7-133">In *PropertyData* è disponibile una dimensione del buffer insufficiente.</span><span class="sxs-lookup"><span data-stu-id="adae7-133">An insufficient buffer size is provided in *propertyData*.</span></span> <span data-ttu-id="adae7-134">Chiamare [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per determinare le dimensioni del buffer *PropertyData* per una determinata proprietà dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="adae7-134">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>|
|<span data-ttu-id="adae7-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="adae7-135">E_POINTER</span></span>|<span data-ttu-id="adae7-136">`nullptr` fornito per *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="adae7-136">`nullptr` was provided for *propertyData*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="adae7-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="adae7-137">Remarks</span></span>

<span data-ttu-id="adae7-138">È possibile chiamare **GetProperty** su un adapter che non è più valido &mdash; . la funzione non avrà esito negativo come conseguenza.</span><span class="sxs-lookup"><span data-stu-id="adae7-138">You can call **GetProperty** on an adapter that's no longer valid&mdash;the function won't fail as a result of that.</span></span> <span data-ttu-id="adae7-139">Questa funzione azzera il buffer *PropertyData* prima di riempirlo.</span><span class="sxs-lookup"><span data-stu-id="adae7-139">This function zeros out the *propertyData* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="adae7-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="adae7-140">See also</span></span>

<span data-ttu-id="adae7-141">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="adae7-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>