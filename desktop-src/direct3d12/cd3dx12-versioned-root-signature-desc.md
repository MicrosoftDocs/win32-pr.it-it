---
title: Struttura CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura desc della firma radice con versione D3D12 \_ \_ .
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- Struttura CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322184"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a><span data-ttu-id="a6fc6-104">\_ \_ \_ Struttura desc della firma radice con versione CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="a6fc6-104">CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="a6fc6-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ desc della \_ firma \_ radice con versione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="a6fc6-105">A helper structure to enable easy initialization of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6fc6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6fc6-106">Syntax</span></span>


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="a6fc6-107">Members</span><span class="sxs-lookup"><span data-stu-id="a6fc6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6fc6-108">**CD3DX12 della \_ \_ firma radice con versione \_ \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-108">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-109">Crea una nuova istanza non inizializzata di una \_ Descrizione della firma radice con versione CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a6fc6-109">Creates a new, uninitialized, instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-110">**firma radice con versione CD3DX12 esplicita \_ \_ \_ \_ DESC (const D3D12 \_ versione \_ radice \_ \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-110">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-111">Crea una nuova istanza di una \_ \_ firma radice CD3DX12 con \_ versione \_ DESC, inizializzata con il contenuto di una struttura della [**\_ \_ \_ firma radice \_ con versione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="a6fc6-111">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-112">**firma radice con versione CD3DX12 esplicita \_ \_ \_ \_ DESC (const D3D12 \_ root \_ Signature \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-112">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-113">Crea una nuova istanza di una \_ \_ firma radice CD3DX12 con \_ versione \_ DESC, inizializzata con il contenuto di una struttura [**D3D12 della \_ \_ firma \_ radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="a6fc6-113">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-114">**firma radice con versione CD3DX12 esplicita \_ \_ \_ \_ DESC (const D3D12 \_ root \_ Signature \_ DESC1 &o)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-114">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-115">Crea una nuova istanza di una \_ \_ firma radice CD3DX12 con \_ versione \_ DESC, inizializzata con il contenuto di una struttura [**\_ \_ \_ DESC1 della firma radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .</span><span class="sxs-lookup"><span data-stu-id="a6fc6-115">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-116">**CD3DX12 della \_ \_ firma radice con versione \_ \_ DESC (uint NUMPARAMETERS, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 firma radice flag Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-116">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-117">Crea una nuova istanza di una \_ Descrizione della firma radice con versione CD3DX12 \_ \_ \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6fc6-117">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="a6fc6-118">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="a6fc6-118">UINT numParameters</span></span>

<span data-ttu-id="a6fc6-119">[**\_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) const \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="a6fc6-119">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="a6fc6-120">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="a6fc6-120">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="a6fc6-121">const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="a6fc6-121">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="a6fc6-122">[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="a6fc6-122">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-123">**CD3DX12 della \_ \_ firma radice con versione \_ \_ DESC (uint NUMPARAMETERS, const D3D12 \_ root \_ parametro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 firma radice flag Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-123">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-124">Crea una nuova istanza di una \_ Descrizione della firma radice con versione CD3DX12 \_ \_ \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6fc6-124">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="a6fc6-125">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="a6fc6-125">UINT numParameters</span></span>

<span data-ttu-id="a6fc6-126">const [**D3D12 \_ radice \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="a6fc6-126">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="a6fc6-127">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="a6fc6-127">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="a6fc6-128">const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="a6fc6-128">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="a6fc6-129">[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="a6fc6-129">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-130">**\_Firma radice con versione CD3DX12 \_ \_ \_ DESC ( \_ impostazione predefinita CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-130">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-131">Crea una nuova istanza di una \_ \_ firma radice CD3DX12 con \_ versione \_ DESC, inizializzata con i parametri predefiniti:</span><span class="sxs-lookup"><span data-stu-id="a6fc6-131">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the default parameters:</span></span>

<span data-ttu-id="a6fc6-132">UINT numParameters = 0</span><span class="sxs-lookup"><span data-stu-id="a6fc6-132">UINT numParameters = 0</span></span>

<span data-ttu-id="a6fc6-133">const [**D3D12 \_ root \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = null</span><span class="sxs-lookup"><span data-stu-id="a6fc6-133">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters = NULL</span></span>

<span data-ttu-id="a6fc6-134">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="a6fc6-134">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="a6fc6-135">const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="a6fc6-135">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="a6fc6-136">[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="a6fc6-136">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-137">**inline init \_ 1 \_ 0 (uint numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint NUMSTATICSAMPLERS = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 root Signature Flags Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-137">**inline Init\_1\_0(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-138">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6fc6-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a6fc6-139">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="a6fc6-139">UINT numParameters</span></span>

<span data-ttu-id="a6fc6-140">[**\_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) const \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="a6fc6-140">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="a6fc6-141">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="a6fc6-141">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="a6fc6-142">const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="a6fc6-142">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="a6fc6-143">[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="a6fc6-143">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-144">**static inline init \_ 1 \_ 0 (D3D12 con \_ versione \_ radice \_ \_ desc &DESC, uint numParameters, const D3D12 \_ root \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 root Signature flag Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-144">**static inline Init\_1\_0(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-145">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6fc6-145">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a6fc6-146">[**D3D12 \_ Descrizione della \_ firma radice con versione \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="a6fc6-146">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="a6fc6-147">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="a6fc6-147">UINT numParameters</span></span>

<span data-ttu-id="a6fc6-148">[**\_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) const \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="a6fc6-148">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="a6fc6-149">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="a6fc6-149">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="a6fc6-150">const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="a6fc6-150">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="a6fc6-151">[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="a6fc6-151">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-152">**inline init \_ 1 \_ 1 (uint numParameters, const D3D12 \_ root \_ parametro1 \* \_ pParameters, uint NUMSTATICSAMPLERS = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ PSTATICSAMPLERS = null, D3D12 firma radice flag Flags \_ \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-152">**inline Init\_1\_1(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-153">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6fc6-153">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a6fc6-154">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="a6fc6-154">UINT numParameters</span></span>

<span data-ttu-id="a6fc6-155">const [**D3D12 \_ radice \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="a6fc6-155">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="a6fc6-156">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="a6fc6-156">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="a6fc6-157">const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="a6fc6-157">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="a6fc6-158">[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="a6fc6-158">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="a6fc6-159">**static inline init \_ 1 \_ 1 (D3D12 della \_ \_ firma radice con versione \_ \_ desc &DESC, uint numParameters, const D3D12 \_ root \_ parametro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sampler \_ desc \* \_ pStaticSamplers = null, D3D12 \_ flag di firma radice Flags \_ \_ = D3D12 \_ root \_ Signature \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-159">**static inline Init\_1\_1(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="a6fc6-160">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6fc6-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="a6fc6-161">[**D3D12 \_ Descrizione della \_ firma radice con versione \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="a6fc6-161">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="a6fc6-162">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="a6fc6-162">UINT numParameters</span></span>

<span data-ttu-id="a6fc6-163">const [**D3D12 \_ radice \_ parametro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="a6fc6-163">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="a6fc6-164">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="a6fc6-164">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="a6fc6-165">const [**D3D12 \_ static \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="a6fc6-165">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="a6fc6-166">[**D3D12 \_ Flag \_ di \_ firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags = D3D12 \_ root \_ Signature \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="a6fc6-166">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6fc6-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6fc6-167">Requirements</span></span>



| <span data-ttu-id="a6fc6-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6fc6-168">Requirement</span></span> | <span data-ttu-id="a6fc6-169">Valore</span><span class="sxs-lookup"><span data-stu-id="a6fc6-169">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fc6-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6fc6-170">Header</span></span><br/> | <dl> <span data-ttu-id="a6fc6-171"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6fc6-171"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6fc6-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6fc6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6fc6-173">**\_ \_ Descrizione della firma radice \_ con versione D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="a6fc6-173">**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="a6fc6-174">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="a6fc6-174">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





