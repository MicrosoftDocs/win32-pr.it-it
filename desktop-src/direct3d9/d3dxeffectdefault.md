---
description: Effetti sui parametri predefiniti.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Struttura D3DXEFFECTDEFAULT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322709"
---
# <a name="d3dxeffectdefault-structure"></a><span data-ttu-id="854f7-103">Struttura D3DXEFFECTDEFAULT</span><span class="sxs-lookup"><span data-stu-id="854f7-103">D3DXEFFECTDEFAULT structure</span></span>

<span data-ttu-id="854f7-104">Effetti sui parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="854f7-104">Effect default parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="854f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="854f7-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a><span data-ttu-id="854f7-106">Members</span><span class="sxs-lookup"><span data-stu-id="854f7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="854f7-107">**pParamName**</span><span class="sxs-lookup"><span data-stu-id="854f7-107">**pParamName**</span></span>
</dt> <dd>

<span data-ttu-id="854f7-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="854f7-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="854f7-109">Nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="854f7-109">Parameter name.</span></span>

</dd> <dt>

<span data-ttu-id="854f7-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="854f7-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="854f7-111">Tipo: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span><span class="sxs-lookup"><span data-stu-id="854f7-111">Type: **[**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="854f7-112">Tipo di dati in pValue.</span><span class="sxs-lookup"><span data-stu-id="854f7-112">Data type in pValue.</span></span> <span data-ttu-id="854f7-113">Per ulteriori informazioni, vedere [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span><span class="sxs-lookup"><span data-stu-id="854f7-113">For more information, see [**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span></span>

</dd> <dt>

<span data-ttu-id="854f7-114">**NumBytes**</span><span class="sxs-lookup"><span data-stu-id="854f7-114">**NumBytes**</span></span>
</dt> <dd>

<span data-ttu-id="854f7-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="854f7-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="854f7-116">Dimensione, in byte, dei dati a cui punta pValue.</span><span class="sxs-lookup"><span data-stu-id="854f7-116">Size, in bytes, of the data pointed to by pValue.</span></span>

</dd> <dt>

<span data-ttu-id="854f7-117">**pValue**</span><span class="sxs-lookup"><span data-stu-id="854f7-117">**pValue**</span></span>
</dt> <dd>

<span data-ttu-id="854f7-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="854f7-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="854f7-119">Puntatore alla posizione di memoria che contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="854f7-119">Pointer to the memory location that contains the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="854f7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="854f7-120">Requirements</span></span>



| <span data-ttu-id="854f7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="854f7-121">Requirement</span></span> | <span data-ttu-id="854f7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="854f7-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="854f7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="854f7-123">Header</span></span><br/> | <dl> <span data-ttu-id="854f7-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="854f7-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="854f7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="854f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="854f7-126">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="854f7-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
