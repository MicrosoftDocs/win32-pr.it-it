---
title: Struttura D3DX11_EFFECT_TYPE_DESC (D3dx11effect. h)
description: Descrive un tipo di variabile di effetto.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- Struttura D3DX11_EFFECT_TYPE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886318"
---
# <a name="d3dx11_effect_type_desc-structure"></a><span data-ttu-id="e82e5-104">\_ \_ Struttura Desc del tipo di effetto D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="e82e5-104">D3DX11\_EFFECT\_TYPE\_DESC structure</span></span>

<span data-ttu-id="e82e5-105">Descrive un tipo di variabile di effetto.</span><span class="sxs-lookup"><span data-stu-id="e82e5-105">Describes an effect-variable type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82e5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e82e5-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a><span data-ttu-id="e82e5-107">Members</span><span class="sxs-lookup"><span data-stu-id="e82e5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e82e5-108">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="e82e5-108">**TypeName**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-110">Nome del tipo, ad esempio "float4" o "struct".</span><span class="sxs-lookup"><span data-stu-id="e82e5-110">Name of the type, for example "float4" or "MyStruct".</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-111">**Classe**</span><span class="sxs-lookup"><span data-stu-id="e82e5-111">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-112">Tipo: **[ **D3D10 \_ \_ \_ classe variabile shader**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-112">Type: **[**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-113">Classe della variabile (vedere [**la \_ classe della \_ variabile \_ shader D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span><span class="sxs-lookup"><span data-stu-id="e82e5-113">The variable class (see [**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e82e5-114">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-115">Tipo: **[ **\_ \_ \_ tipo di variabile shader D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-115">Type: **[**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-116">Tipo di variabile (vedere [**il \_ tipo di \_ variabile \_ shader D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span><span class="sxs-lookup"><span data-stu-id="e82e5-116">The variable type (see [**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-117">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="e82e5-117">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-119">Numero di elementi in questo tipo (0 se non è una matrice).</span><span class="sxs-lookup"><span data-stu-id="e82e5-119">Number of elements in this type (0 if not an array).</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-120">**Members**</span><span class="sxs-lookup"><span data-stu-id="e82e5-120">**Members**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-122">Numero di membri (0 se non è una struttura).</span><span class="sxs-lookup"><span data-stu-id="e82e5-122">Number of members (0 if not a structure).</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-123">**prime righe**</span><span class="sxs-lookup"><span data-stu-id="e82e5-123">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-125">Numero di righe in questo tipo (0 se non è una primitiva numerica).</span><span class="sxs-lookup"><span data-stu-id="e82e5-125">Number of rows in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-126">**Colonne**</span><span class="sxs-lookup"><span data-stu-id="e82e5-126">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-127">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-128">Numero di colonne in questo tipo (0 se non è una primitiva numerica).</span><span class="sxs-lookup"><span data-stu-id="e82e5-128">Number of columns in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-129">**PackedSize**</span><span class="sxs-lookup"><span data-stu-id="e82e5-129">**PackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-131">Numero di byte necessari per rappresentare questo tipo di dati, quando è strettamente compresso.</span><span class="sxs-lookup"><span data-stu-id="e82e5-131">Number of bytes required to represent this data type, when tightly packed.</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-132">**UnpackedSize**</span><span class="sxs-lookup"><span data-stu-id="e82e5-132">**UnpackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-134">Numero di byte occupati da questo tipo di dati, quando sono disposti in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="e82e5-134">Number of bytes occupied by this data type, when laid out in a constant buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e82e5-135">**Stride**</span><span class="sxs-lookup"><span data-stu-id="e82e5-135">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="e82e5-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e82e5-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e82e5-137">Numero di byte da cercare tra gli elementi, quando sono disposti in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="e82e5-137">Number of bytes to seek between elements, when laid out in a constant buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e82e5-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="e82e5-138">Remarks</span></span>

<span data-ttu-id="e82e5-139">Il \_ \_ tipo di effetto D3DX11 \_ desc viene usato con [ **ID3DX11EffectType:: getdesc**](id3dx11effecttype-getdesc.md)</span><span class="sxs-lookup"><span data-stu-id="e82e5-139">D3DX11\_EFFECT\_TYPE\_DESC is used with [**ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="e82e5-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e82e5-140">Requirements</span></span>



| <span data-ttu-id="e82e5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e82e5-141">Requirement</span></span> | <span data-ttu-id="e82e5-142">Valore</span><span class="sxs-lookup"><span data-stu-id="e82e5-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e82e5-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e82e5-143">Header</span></span><br/> | <dl> <span data-ttu-id="e82e5-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e82e5-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e82e5-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e82e5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82e5-146">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="e82e5-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

