---
description: Descrive una tecnica utilizzata da un effetto.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: Struttura D3DXTECHNIQUE_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058598"
---
# <a name="d3dxtechnique_desc-structure"></a><span data-ttu-id="67286-103">\_Struttura D3DXTECHNIQUE DESC</span><span class="sxs-lookup"><span data-stu-id="67286-103">D3DXTECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="67286-104">Descrive una tecnica utilizzata da un effetto.</span><span class="sxs-lookup"><span data-stu-id="67286-104">Describes a technique used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="67286-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67286-105">Syntax</span></span>


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="67286-106">Members</span><span class="sxs-lookup"><span data-stu-id="67286-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="67286-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="67286-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="67286-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67286-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67286-109">Stringa che contiene il nome della tecnica.</span><span class="sxs-lookup"><span data-stu-id="67286-109">String that contains the technique name.</span></span>

</dd> <dt>

<span data-ttu-id="67286-110">**Passa**</span><span class="sxs-lookup"><span data-stu-id="67286-110">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="67286-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67286-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67286-112">Numero di passaggi di rendering necessari per la tecnica.</span><span class="sxs-lookup"><span data-stu-id="67286-112">Number of rendering passes the technique requires.</span></span> <span data-ttu-id="67286-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="67286-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="67286-114">**annotazioni**</span><span class="sxs-lookup"><span data-stu-id="67286-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="67286-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67286-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67286-116">Numero di annotazioni.</span><span class="sxs-lookup"><span data-stu-id="67286-116">The number of annotations.</span></span> <span data-ttu-id="67286-117">Vedere [aggiungere informazioni ai parametri di effetto con le \_ annotazioni](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="67286-117">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67286-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="67286-118">Remarks</span></span>

<span data-ttu-id="67286-119">Alcune schede video possono eseguire il rendering di due trame in un singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="67286-119">Some video cards can render two textures in a single pass.</span></span> <span data-ttu-id="67286-120">Tuttavia, se una scheda non dispone di questa funzionalità, spesso è possibile eseguire il rendering dello stesso effetto in due passaggi, usando una trama per ogni passaggio.</span><span class="sxs-lookup"><span data-stu-id="67286-120">However, if a card does not have this capability, it is often possible to render the same effect in two passes, using one texture for each pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="67286-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67286-121">Requirements</span></span>



| <span data-ttu-id="67286-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="67286-122">Requirement</span></span> | <span data-ttu-id="67286-123">Valore</span><span class="sxs-lookup"><span data-stu-id="67286-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="67286-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67286-124">Header</span></span><br/> | <dl> <span data-ttu-id="67286-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="67286-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67286-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67286-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67286-127">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="67286-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
