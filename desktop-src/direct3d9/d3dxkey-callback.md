---
description: Descrive una chiave di callback da usare nell'animazione del fotogramma chiave.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: Struttura D3DXKEY_CALLBACK (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322643"
---
# <a name="d3dxkey_callback-structure"></a><span data-ttu-id="bdbf4-103">\_Struttura di callback D3DXKEY</span><span class="sxs-lookup"><span data-stu-id="bdbf4-103">D3DXKEY\_CALLBACK structure</span></span>

<span data-ttu-id="bdbf4-104">Descrive una chiave di callback da usare nell'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-104">Describes a callback key for use in key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdbf4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdbf4-105">Syntax</span></span>


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a><span data-ttu-id="bdbf4-106">Members</span><span class="sxs-lookup"><span data-stu-id="bdbf4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bdbf4-107">**Time**</span><span class="sxs-lookup"><span data-stu-id="bdbf4-107">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="bdbf4-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bdbf4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bdbf4-109">Timestamp del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-109">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="bdbf4-110">**pCallbackData**</span><span class="sxs-lookup"><span data-stu-id="bdbf4-110">**pCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="bdbf4-111">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bdbf4-111">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bdbf4-112">Puntatore ai dati di callback utente.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-112">Pointer to user callback data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdbf4-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdbf4-113">Requirements</span></span>



| <span data-ttu-id="bdbf4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdbf4-114">Requirement</span></span> | <span data-ttu-id="bdbf4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bdbf4-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbf4-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdbf4-116">Header</span></span><br/> | <dl> <span data-ttu-id="bdbf4-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdbf4-117"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdbf4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdbf4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbf4-119">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="bdbf4-119">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
