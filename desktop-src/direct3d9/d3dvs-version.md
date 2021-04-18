---
description: Creare un token di numero di versione del vertex shader.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: D3DVS_VERSION macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323021"
---
# <a name="d3dvs_version-macro"></a><span data-ttu-id="e63c7-103">D3DVS \_ versione macro</span><span class="sxs-lookup"><span data-stu-id="e63c7-103">D3DVS\_VERSION macro</span></span>

<span data-ttu-id="e63c7-104">Creare un token di numero di versione del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e63c7-104">Create a vertex shader version number token.</span></span>

## <a name="syntax"></a><span data-ttu-id="e63c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e63c7-105">Syntax</span></span>


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="e63c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e63c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e63c7-107">*\_Principali*</span><span class="sxs-lookup"><span data-stu-id="e63c7-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="e63c7-108">Versione principale del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e63c7-108">The major vertex shader version.</span></span> <span data-ttu-id="e63c7-109">Vedere la sezione Osservazioni per i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="e63c7-109">See remarks for appropriate values.</span></span>

</dd> <dt>

<span data-ttu-id="e63c7-110">*\_Minorenne*</span><span class="sxs-lookup"><span data-stu-id="e63c7-110">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="e63c7-111">Versione del vertex shader secondaria.</span><span class="sxs-lookup"><span data-stu-id="e63c7-111">The minor vertex shader version.</span></span> <span data-ttu-id="e63c7-112">Vedere la sezione Osservazioni per i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="e63c7-112">See remarks for appropriate values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e63c7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e63c7-113">Return value</span></span>

<span data-ttu-id="e63c7-114">Restituisce un valore DWORD che è una versione del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e63c7-114">Returns a DWORD value that is a vertex shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="e63c7-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e63c7-115">Remarks</span></span>

<span data-ttu-id="e63c7-116">Numeri di versione</span><span class="sxs-lookup"><span data-stu-id="e63c7-116">Version Numbers</span></span>

<span data-ttu-id="e63c7-117">Il numero di versione è una combinazione della versione principale e dei numeri di versione di vertex shader secondari.</span><span class="sxs-lookup"><span data-stu-id="e63c7-117">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="e63c7-118">I numeri validi sono visualizzati nella tabella.</span><span class="sxs-lookup"><span data-stu-id="e63c7-118">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="e63c7-119">Principale</span><span class="sxs-lookup"><span data-stu-id="e63c7-119">Major</span></span> | <span data-ttu-id="e63c7-120">Minorenne</span><span class="sxs-lookup"><span data-stu-id="e63c7-120">Minor</span></span> | <span data-ttu-id="e63c7-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="e63c7-121">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="e63c7-122">1</span><span class="sxs-lookup"><span data-stu-id="e63c7-122">1</span></span>     | <span data-ttu-id="e63c7-123">1</span><span class="sxs-lookup"><span data-stu-id="e63c7-123">1</span></span>     | <span data-ttu-id="e63c7-124">\_Versione di D3DVS (1,1)</span><span class="sxs-lookup"><span data-stu-id="e63c7-124">D3DVS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="e63c7-125">2</span><span class="sxs-lookup"><span data-stu-id="e63c7-125">2</span></span>     | <span data-ttu-id="e63c7-126">0</span><span class="sxs-lookup"><span data-stu-id="e63c7-126">0</span></span>     | <span data-ttu-id="e63c7-127">\_Versione di D3DVS (2, 0)</span><span class="sxs-lookup"><span data-stu-id="e63c7-127">D3DVS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="e63c7-128">3</span><span class="sxs-lookup"><span data-stu-id="e63c7-128">3</span></span>     | <span data-ttu-id="e63c7-129">0</span><span class="sxs-lookup"><span data-stu-id="e63c7-129">0</span></span>     | <span data-ttu-id="e63c7-130">\_Versione di D3DVS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="e63c7-130">D3DVS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e63c7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e63c7-131">Requirements</span></span>



| <span data-ttu-id="e63c7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e63c7-132">Requirement</span></span> | <span data-ttu-id="e63c7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e63c7-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e63c7-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e63c7-134">Header</span></span><br/> | <dl> <span data-ttu-id="e63c7-135"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e63c7-135"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e63c7-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e63c7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e63c7-137">Macro</span><span class="sxs-lookup"><span data-stu-id="e63c7-137">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




