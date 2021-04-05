---
description: Descrive un oggetto effetto.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: Struttura D3DXEFFECT_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762053"
---
# <a name="d3dxeffect_desc-structure"></a><span data-ttu-id="c61f1-103">\_Struttura D3DXEFFECT DESC</span><span class="sxs-lookup"><span data-stu-id="c61f1-103">D3DXEFFECT\_DESC structure</span></span>

<span data-ttu-id="c61f1-104">Descrive un oggetto effetto.</span><span class="sxs-lookup"><span data-stu-id="c61f1-104">Describes an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c61f1-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="c61f1-106">Members</span><span class="sxs-lookup"><span data-stu-id="c61f1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c61f1-107">**Autore**</span><span class="sxs-lookup"><span data-stu-id="c61f1-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="c61f1-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c61f1-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c61f1-109">Stringa che contiene il nome dell'autore dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="c61f1-109">String that contains the name of the effect creator.</span></span>

</dd> <dt>

<span data-ttu-id="c61f1-110">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="c61f1-110">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="c61f1-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c61f1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c61f1-112">Numero di parametri utilizzati per effetto.</span><span class="sxs-lookup"><span data-stu-id="c61f1-112">Number of parameters used for effect.</span></span>

</dd> <dt>

<span data-ttu-id="c61f1-113">**Tecniche**</span><span class="sxs-lookup"><span data-stu-id="c61f1-113">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="c61f1-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c61f1-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c61f1-115">Numero di tecniche che consentono di eseguire il rendering dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="c61f1-115">Number of techniques that can render the effect.</span></span>

</dd> <dt>

<span data-ttu-id="c61f1-116">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="c61f1-116">**Functions**</span></span>
</dt> <dd>

<span data-ttu-id="c61f1-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c61f1-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c61f1-118">Numero di funzioni che possono eseguire il rendering dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="c61f1-118">Number of functions that can render the effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c61f1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c61f1-119">Remarks</span></span>

<span data-ttu-id="c61f1-120">Un oggetto Effect può contenere più tecniche di rendering e parametri per lo stesso effetto.</span><span class="sxs-lookup"><span data-stu-id="c61f1-120">An effect object can contain multiple rendering techniques and parameters for the same effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="c61f1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c61f1-121">Requirements</span></span>



| <span data-ttu-id="c61f1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c61f1-122">Requirement</span></span> | <span data-ttu-id="c61f1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c61f1-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c61f1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c61f1-124">Header</span></span><br/> | <dl> <span data-ttu-id="c61f1-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c61f1-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61f1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c61f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61f1-127">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="c61f1-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
