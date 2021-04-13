---
description: Tipo di dati per la gestione di un set di parametri effetti predefiniti.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: Struttura D3DXEFFECTINSTANCE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354884"
---
# <a name="d3dxeffectinstance-structure"></a><span data-ttu-id="a3c2a-103">Struttura D3DXEFFECTINSTANCE</span><span class="sxs-lookup"><span data-stu-id="a3c2a-103">D3DXEFFECTINSTANCE structure</span></span>

<span data-ttu-id="a3c2a-104">Tipo di dati per la gestione di un set di parametri effetti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a3c2a-104">Data type for managing a set of default effect parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c2a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3c2a-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a><span data-ttu-id="a3c2a-106">Members</span><span class="sxs-lookup"><span data-stu-id="a3c2a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3c2a-107">**pEffectFilename**</span><span class="sxs-lookup"><span data-stu-id="a3c2a-107">**pEffectFilename**</span></span>
</dt> <dd>

<span data-ttu-id="a3c2a-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="a3c2a-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a3c2a-109">Nome del file di effetti.</span><span class="sxs-lookup"><span data-stu-id="a3c2a-109">Name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="a3c2a-110">**NumDefaults**</span><span class="sxs-lookup"><span data-stu-id="a3c2a-110">**NumDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="a3c2a-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3c2a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3c2a-112">Numero di parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a3c2a-112">Number of default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="a3c2a-113">**pDefaults**</span><span class="sxs-lookup"><span data-stu-id="a3c2a-113">**pDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="a3c2a-114">Tipo: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span><span class="sxs-lookup"><span data-stu-id="a3c2a-114">Type: **[**LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a3c2a-115">Puntatore a una matrice di elementi [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , ognuno dei quali contiene un parametro Effect.</span><span class="sxs-lookup"><span data-stu-id="a3c2a-115">Pointer to an array of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) elements, each of which contains an effect parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3c2a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3c2a-116">Requirements</span></span>



| <span data-ttu-id="a3c2a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3c2a-117">Requirement</span></span> | <span data-ttu-id="a3c2a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a3c2a-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c2a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3c2a-119">Header</span></span><br/> | <dl> <span data-ttu-id="a3c2a-120"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3c2a-120"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3c2a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3c2a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3c2a-122">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="a3c2a-122">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
