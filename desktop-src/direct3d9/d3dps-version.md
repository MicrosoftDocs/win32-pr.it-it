---
description: Creare un token di versione di pixel shader.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: D3DPS_VERSION macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355049"
---
# <a name="d3dps_version-macro"></a><span data-ttu-id="068e9-103">D3DPS \_ versione macro</span><span class="sxs-lookup"><span data-stu-id="068e9-103">D3DPS\_VERSION macro</span></span>

<span data-ttu-id="068e9-104">Creare un token di versione di pixel shader.</span><span class="sxs-lookup"><span data-stu-id="068e9-104">Create a pixel shader version token.</span></span>

## <a name="syntax"></a><span data-ttu-id="068e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="068e9-105">Syntax</span></span>


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="068e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="068e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="068e9-107">*\_Principali*</span><span class="sxs-lookup"><span data-stu-id="068e9-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="068e9-108">Versione principale del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="068e9-108">The major pixel shader version.</span></span>

</dd> <dt>

<span data-ttu-id="068e9-109">*\_Minorenne*</span><span class="sxs-lookup"><span data-stu-id="068e9-109">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="068e9-110">Versione secondaria del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="068e9-110">The minor pixel shader version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="068e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="068e9-111">Return value</span></span>

<span data-ttu-id="068e9-112">Restituisce un valore DWORD che è una versione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="068e9-112">Returns a DWORD value that is a pixel shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="068e9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="068e9-113">Remarks</span></span>

<span data-ttu-id="068e9-114">Numeri di versione</span><span class="sxs-lookup"><span data-stu-id="068e9-114">Version Numbers</span></span>

<span data-ttu-id="068e9-115">Il numero di versione è una combinazione della versione principale e dei numeri di versione di vertex shader secondari.</span><span class="sxs-lookup"><span data-stu-id="068e9-115">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="068e9-116">I numeri validi sono visualizzati nella tabella.</span><span class="sxs-lookup"><span data-stu-id="068e9-116">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="068e9-117">Principale</span><span class="sxs-lookup"><span data-stu-id="068e9-117">Major</span></span> | <span data-ttu-id="068e9-118">Minorenne</span><span class="sxs-lookup"><span data-stu-id="068e9-118">Minor</span></span> | <span data-ttu-id="068e9-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="068e9-119">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="068e9-120">1</span><span class="sxs-lookup"><span data-stu-id="068e9-120">1</span></span>     | <span data-ttu-id="068e9-121">1</span><span class="sxs-lookup"><span data-stu-id="068e9-121">1</span></span>     | <span data-ttu-id="068e9-122">\_Versione di D3DPS (1,1)</span><span class="sxs-lookup"><span data-stu-id="068e9-122">D3DPS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="068e9-123">1</span><span class="sxs-lookup"><span data-stu-id="068e9-123">1</span></span>     | <span data-ttu-id="068e9-124">2</span><span class="sxs-lookup"><span data-stu-id="068e9-124">2</span></span>     | <span data-ttu-id="068e9-125">\_Versione di D3DPS (1, 2)</span><span class="sxs-lookup"><span data-stu-id="068e9-125">D3DPS\_VERSION(1,2)</span></span> |
| <span data-ttu-id="068e9-126">1</span><span class="sxs-lookup"><span data-stu-id="068e9-126">1</span></span>     | <span data-ttu-id="068e9-127">3</span><span class="sxs-lookup"><span data-stu-id="068e9-127">3</span></span>     | <span data-ttu-id="068e9-128">\_Versione di D3DPS (1,3)</span><span class="sxs-lookup"><span data-stu-id="068e9-128">D3DPS\_VERSION(1,3)</span></span> |
| <span data-ttu-id="068e9-129">1</span><span class="sxs-lookup"><span data-stu-id="068e9-129">1</span></span>     | <span data-ttu-id="068e9-130">4</span><span class="sxs-lookup"><span data-stu-id="068e9-130">4</span></span>     | <span data-ttu-id="068e9-131">\_Versione di D3DPS (1,4)</span><span class="sxs-lookup"><span data-stu-id="068e9-131">D3DPS\_VERSION(1,4)</span></span> |
| <span data-ttu-id="068e9-132">2</span><span class="sxs-lookup"><span data-stu-id="068e9-132">2</span></span>     | <span data-ttu-id="068e9-133">0</span><span class="sxs-lookup"><span data-stu-id="068e9-133">0</span></span>     | <span data-ttu-id="068e9-134">\_Versione di D3DPS (2, 0)</span><span class="sxs-lookup"><span data-stu-id="068e9-134">D3DPS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="068e9-135">3</span><span class="sxs-lookup"><span data-stu-id="068e9-135">3</span></span>     | <span data-ttu-id="068e9-136">0</span><span class="sxs-lookup"><span data-stu-id="068e9-136">0</span></span>     | <span data-ttu-id="068e9-137">\_Versione di D3DPS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="068e9-137">D3DPS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="068e9-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="068e9-138">Requirements</span></span>



| <span data-ttu-id="068e9-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="068e9-139">Requirement</span></span> | <span data-ttu-id="068e9-140">Valore</span><span class="sxs-lookup"><span data-stu-id="068e9-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="068e9-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="068e9-141">Header</span></span><br/> | <dl> <span data-ttu-id="068e9-142"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="068e9-142"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="068e9-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="068e9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068e9-144">Macro</span><span class="sxs-lookup"><span data-stu-id="068e9-144">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="068e9-145">D3DCAPS9</span><span class="sxs-lookup"><span data-stu-id="068e9-145">D3DCAPS9</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




