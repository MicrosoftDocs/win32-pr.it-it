---
title: Struttura D3DX11_EFFECT_DESC (D3dx11effect. h)
description: Descrive un effetto.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- Struttura D3DX11_EFFECT_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982587"
---
# <a name="d3dx11_effect_desc-structure"></a><span data-ttu-id="b4494-104">D3DX11 \_ effetto \_ desc struttura</span><span class="sxs-lookup"><span data-stu-id="b4494-104">D3DX11\_EFFECT\_DESC structure</span></span>

<span data-ttu-id="b4494-105">Descrive un effetto.</span><span class="sxs-lookup"><span data-stu-id="b4494-105">Describes an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4494-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4494-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="b4494-107">Members</span><span class="sxs-lookup"><span data-stu-id="b4494-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4494-108">**ConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="b4494-108">**ConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b4494-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4494-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b4494-110">Numero di buffer costanti in questo effetto.</span><span class="sxs-lookup"><span data-stu-id="b4494-110">Number of constant buffers in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="b4494-111">**GlobalVariables**</span><span class="sxs-lookup"><span data-stu-id="b4494-111">**GlobalVariables**</span></span>
</dt> <dd>

<span data-ttu-id="b4494-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4494-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b4494-113">Numero di variabili globali in questo effetto.</span><span class="sxs-lookup"><span data-stu-id="b4494-113">Number of global variables in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="b4494-114">**InterfaceVariables**</span><span class="sxs-lookup"><span data-stu-id="b4494-114">**InterfaceVariables**</span></span>
</dt> <dd>

<span data-ttu-id="b4494-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4494-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b4494-116">Numero di interfacce globali in questo effetto.</span><span class="sxs-lookup"><span data-stu-id="b4494-116">Number of global interfaces in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="b4494-117">**Tecniche**</span><span class="sxs-lookup"><span data-stu-id="b4494-117">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="b4494-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4494-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b4494-119">Numero di tecniche in questo effetto.</span><span class="sxs-lookup"><span data-stu-id="b4494-119">Number of techniques in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="b4494-120">**Gruppi**</span><span class="sxs-lookup"><span data-stu-id="b4494-120">**Groups**</span></span>
</dt> <dd>

<span data-ttu-id="b4494-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4494-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b4494-122">Numero di gruppi in questo effetto.</span><span class="sxs-lookup"><span data-stu-id="b4494-122">Number of groups in this effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4494-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4494-123">Remarks</span></span>

<span data-ttu-id="b4494-124">D3DX11 \_ Effect \_ desc viene usato con [**ID3DX11Effect:: getdesc**](id3dx11effect-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="b4494-124">D3DX11\_EFFECT\_DESC is used with [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4494-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4494-125">Requirements</span></span>



| <span data-ttu-id="b4494-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4494-126">Requirement</span></span> | <span data-ttu-id="b4494-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b4494-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4494-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4494-128">Header</span></span><br/> | <dl> <span data-ttu-id="b4494-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4494-129"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4494-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4494-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4494-131">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="b4494-131">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

