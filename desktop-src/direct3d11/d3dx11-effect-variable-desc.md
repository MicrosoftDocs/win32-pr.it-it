---
title: Struttura D3DX11_EFFECT_VARIABLE_DESC (D3dx11effect. h)
description: Descrive una variabile di effetto.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- Struttura D3DX11_EFFECT_VARIABLE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996204"
---
# <a name="d3dx11_effect_variable_desc-structure"></a><span data-ttu-id="bbfb2-104">\_ \_ Struttura desc della variabile di effetto D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="bbfb2-104">D3DX11\_EFFECT\_VARIABLE\_DESC structure</span></span>

<span data-ttu-id="bbfb2-105">Descrive una variabile di effetto.</span><span class="sxs-lookup"><span data-stu-id="bbfb2-105">Describes an effect variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfb2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbfb2-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="bbfb2-107">Members</span><span class="sxs-lookup"><span data-stu-id="bbfb2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bbfb2-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="bbfb2-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="bbfb2-110">Nome della variabile, dell'annotazione o del membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="bbfb2-110">Name of this variable, annotation, or structure member.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb2-111">**Semantica**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-111">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="bbfb2-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="bbfb2-113">Stringa semantica di questa variabile o membro della struttura (NULL per le annotazioni o se non è presente).</span><span class="sxs-lookup"><span data-stu-id="bbfb2-113">Semantic string of this variable or structure member (NULL for annotations or if not present).</span></span>

</dd> <dt>

<span data-ttu-id="bbfb2-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="bbfb2-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="bbfb2-116">Flag facoltativi per le variabili di effetto.</span><span class="sxs-lookup"><span data-stu-id="bbfb2-116">Optional flags for effect variables.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb2-117">**annotazioni**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-117">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="bbfb2-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="bbfb2-119">Numero di annotazioni sulla variabile (sempre 0 per le annotazioni).</span><span class="sxs-lookup"><span data-stu-id="bbfb2-119">Number of annotations on this variable (always 0 for annotations).</span></span>

</dd> <dt>

<span data-ttu-id="bbfb2-120">**BufferOffset**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-120">**BufferOffset**</span></span>
</dt> <dd>

<span data-ttu-id="bbfb2-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="bbfb2-122">Offset in che contiene cbuffer o tbuffer (sempre 0 per le annotazioni o le variabili non nei buffer costanti).</span><span class="sxs-lookup"><span data-stu-id="bbfb2-122">Offset into containing cbuffer or tbuffer (always 0 for annotations or variables not in constant buffers).</span></span>

</dd> <dt>

<span data-ttu-id="bbfb2-123">**ExplicitBindPoint**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-123">**ExplicitBindPoint**</span></span>
</dt> <dd>

<span data-ttu-id="bbfb2-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bbfb2-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="bbfb2-125">Utilizzato se la variabile è stata associata in modo esplicito tramite la parola chiave register.</span><span class="sxs-lookup"><span data-stu-id="bbfb2-125">Used if the variable has been explicitly bound using the register keyword.</span></span> <span data-ttu-id="bbfb2-126">Flag di controllo per \_ il \_ \_ punto di binding esplicito della variabile di effetto D3DX11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bbfb2-126">Check Flags for D3DX11\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbfb2-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbfb2-127">Remarks</span></span>

<span data-ttu-id="bbfb2-128">La \_ \_ variabile di effetto D3DX11 \_ desc viene usata con [**ID3DX11EffectVariable:: getdesc**](id3dx11effectvariable-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="bbfb2-128">D3DX11\_EFFECT\_VARIABLE\_DESC is used with [**ID3DX11EffectVariable::GetDesc**](id3dx11effectvariable-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbfb2-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbfb2-129">Requirements</span></span>



| <span data-ttu-id="bbfb2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbfb2-130">Requirement</span></span> | <span data-ttu-id="bbfb2-131">Valore</span><span class="sxs-lookup"><span data-stu-id="bbfb2-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbfb2-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbfb2-132">Header</span></span><br/> | <dl> <span data-ttu-id="bbfb2-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbfb2-133"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbfb2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbfb2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbfb2-135">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="bbfb2-135">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

