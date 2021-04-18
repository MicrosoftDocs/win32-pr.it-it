---
title: Struttura CD3DX12_CPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura di handle del descrittore della CPU D3D12 \_ .
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- Struttura CD3DX12_CPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1045202c531aa200745fc89ed067628a175486
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322280"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a><span data-ttu-id="cd6ad-104">\_Struttura dell' \_ handle del descrittore della CPU CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="cd6ad-104">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="cd6ad-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="cd6ad-105">A helper structure to enable easy initialization of a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6ad-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd6ad-106">Syntax</span></span>


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="cd6ad-107">Members</span><span class="sxs-lookup"><span data-stu-id="cd6ad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd6ad-108">**\_ \_ Handle descrittore CPU CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-108">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-109">Crea una nuova istanza non inizializzata di un \_ \_ handle del descrittore della CPU CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="cd6ad-109">Creates a new, uninitialized, instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-110">**handle del \_ descrittore della CPU CD3DX12 esplicito \_ \_ (const D3D12 \_ CPU \_ \_ handle &o)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-110">**explicit CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-111">Crea una nuova istanza di un \_ \_ handle descrittore della CPU CD3DX12 \_ , inizializzato con il contenuto di un'altra struttura dell' [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="cd6ad-111">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-112">**\_ \_ Handle descrittore CPU CD3DX12 \_ ( \_ impostazione predefinita CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-112">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-113">Crea una nuova istanza di un \_ \_ handle descrittore della CPU CD3DX12 \_ , inizializzato con parametri predefiniti (puntatore impostato su zero).</span><span class="sxs-lookup"><span data-stu-id="cd6ad-113">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (pointer set to zero).</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-114">**\_ \_ Handle descrittore CPU CD3DX12 \_ (const D3D12 \_ CPU \_ descrittore \_ handle &other, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-114">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-115">Crea una nuova istanza di un \_ \_ handle descrittore della CPU CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd6ad-115">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="cd6ad-116">\_ \_ Handle descrittore CPU D3D12 \_ &altro</span><span class="sxs-lookup"><span data-stu-id="cd6ad-116">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="cd6ad-117">INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-118">**\_ \_ Handle descrittore CPU CD3DX12 \_ (const D3D12 \_ CPU \_ descrittore \_ handle &other, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-118">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-119">Crea una nuova istanza di un \_ \_ handle descrittore della CPU CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd6ad-119">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="cd6ad-120">\_ \_ Handle descrittore CPU D3D12 \_ &altro</span><span class="sxs-lookup"><span data-stu-id="cd6ad-120">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="cd6ad-121">INT offsetInDescriptors: numero di descrittori in base a cui incrementare.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="cd6ad-122">UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-123">**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-124">Imposta l'offset in base al numero specificato di descrittori e alla quantità di incremento per ogni descrittore.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="cd6ad-125">USA i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd6ad-125">Uses the following parameters:</span></span>

<span data-ttu-id="cd6ad-126">INT offsetInDescriptors: numero di descrittori in base a cui incrementare.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="cd6ad-127">UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-128">**Offset (INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-129">Imposta l'offset in base al numero di incrementi specificato.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="cd6ad-130">USA i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd6ad-130">Uses the following parameters:</span></span>

<span data-ttu-id="cd6ad-131">INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-132">**operator = = ( \_ in \_ const D3D12 \_ CPU \_ descrittore \_ handle& altro) const**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-132">**operator==( \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-133">Verifica l'uguaglianza tra l'handle descrittore della CPU CD3DX12 corrente e l'handle descrittore della CPU \_ \_ \_ D3D12 specificato \_ \_ o l' \_ \_ \_ handle del descrittore della CPU CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="cd6ad-133">Tests for equality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-134">**operator! = ( \_ in \_ const D3D12 \_ CPU \_ descrittore \_ handle& altro) const**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-134">**operator!=(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-135">Verifica la disuguaglianza tra l'handle descrittore della CPU CD3DX12 corrente e l'handle del descrittore della CPU \_ \_ \_ D3D12 specificato \_ o l'handle del \_ \_ \_ \_ descrittore della CPU CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="cd6ad-135">Tests for inequality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-136">**operator = (const D3D12 \_ CPU \_ descrittore \_ handle &altro)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-136">**operator=(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-137">Imposta l'handle del descrittore della CPU CD3DX12 corrente sugli stessi valori dell'handle del descrittore della CPU \_ \_ \_ D3D12 specificato \_ o dell'handle del \_ \_ \_ \_ descrittore della CPU CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="cd6ad-137">Sets the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-138">**inline InitOffsetted ( \_ in \_ const D3D12 \_ CPU \_ descrittore \_ handle &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-138">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-139">Inizializza una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con il numero specificato di elementi.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-139">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="cd6ad-140">USA i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd6ad-140">Uses the following parameters:</span></span>

<span data-ttu-id="cd6ad-141">\_In \_ const D3D12 \_ CPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-141">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="cd6ad-142">INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-143">**inline InitOffsetted ( \_ in \_ const D3D12 \_ CPU \_ descrittore \_ handle &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-143">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-144">Inizializza una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-144">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="cd6ad-145">USA i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd6ad-145">Uses the following parameters:</span></span>

<span data-ttu-id="cd6ad-146">\_In \_ const D3D12 \_ CPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-146">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="cd6ad-147">INT offsetInDescriptors: numero di descrittori in base a cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="cd6ad-148">UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-149">**static inline InitOffsetted ( \_ out \_ D3D12 \_ CPU \_ descrittore handle \_ &handle, \_ in \_ const D3D12 \_ CPU \_ descrittore handle \_ &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-149">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-150">Inizializza una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-150">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="cd6ad-151">USA i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd6ad-151">Uses the following parameters:</span></span>

<span data-ttu-id="cd6ad-152">\_Handle \_ \_ \_ del descrittore della cpu out D3D12 &handle \_ : restituisce l' \_ \_ handle descrittore della CPU D3D12 risultante \_ .</span><span class="sxs-lookup"><span data-stu-id="cd6ad-152">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="cd6ad-153">\_In \_ const D3D12 \_ CPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-153">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="cd6ad-154">INT offsetScaledByIncrementSize: numero di incrementi in base a cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="cd6ad-155">**static inline InitOffsetted ( \_ out \_ D3D12 \_ CPU \_ descrittore handle \_ &handle, \_ in \_ const D3D12 \_ CPU \_ descrittore handle \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="cd6ad-155">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cd6ad-156">Inizializza una struttura di [**\_ \_ \_ handle del descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un offset, usando il numero specificato di descrittori della dimensione specificata.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-156">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="cd6ad-157">USA i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd6ad-157">Uses the following parameters:</span></span>

<span data-ttu-id="cd6ad-158">\_Handle \_ \_ \_ del descrittore della cpu out D3D12 &handle \_ : restituisce l' \_ \_ handle descrittore della CPU D3D12 risultante \_ .</span><span class="sxs-lookup"><span data-stu-id="cd6ad-158">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="cd6ad-159">\_In \_ const D3D12 \_ CPU \_ descrittor \_ handle &base: l'indirizzo di base da cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-159">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="cd6ad-160">INT offsetInDescriptors: numero di descrittori in base a cui eseguire l'offset.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="cd6ad-161">UINT descriptorIncrementSize: valore in base al quale incrementare per ogni descrittore, inclusa la spaziatura interna.</span><span class="sxs-lookup"><span data-stu-id="cd6ad-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd6ad-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd6ad-162">Requirements</span></span>



| <span data-ttu-id="cd6ad-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd6ad-163">Requirement</span></span> | <span data-ttu-id="cd6ad-164">Valore</span><span class="sxs-lookup"><span data-stu-id="cd6ad-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6ad-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd6ad-165">Header</span></span><br/> | <dl> <span data-ttu-id="cd6ad-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd6ad-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd6ad-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd6ad-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6ad-168">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="cd6ad-168">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





