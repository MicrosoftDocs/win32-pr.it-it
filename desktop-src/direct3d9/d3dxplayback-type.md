---
description: Definisce il tipo di modalità di ciclo del set di animazioni utilizzato per la riproduzione.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: Enumerazione D3DXPLAYBACK_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ce95b4765ec678c43c8e0ed92008deeb9927298
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886277"
---
# <a name="d3dxplayback_type-enumeration"></a><span data-ttu-id="c9b52-103">\_Enumerazione del tipo D3DXPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="c9b52-103">D3DXPLAYBACK\_TYPE enumeration</span></span>

<span data-ttu-id="c9b52-104">Definisce il tipo di modalità di ciclo del set di animazioni utilizzato per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c9b52-104">Defines the type of animation set looping modes used for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9b52-105">Syntax</span></span>


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c9b52-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c9b52-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c9b52-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**\_Ciclo D3DXPLAY**</span><span class="sxs-lookup"><span data-stu-id="c9b52-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY\_LOOP**</span></span>
</dt> <dd>

<span data-ttu-id="c9b52-108">L'animazione si ripete all'infinito.</span><span class="sxs-lookup"><span data-stu-id="c9b52-108">The animation repeats endlessly.</span></span>

</dd> <dt>

<span data-ttu-id="c9b52-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ una volta**</span><span class="sxs-lookup"><span data-stu-id="c9b52-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY\_ONCE**</span></span>
</dt> <dd>

<span data-ttu-id="c9b52-110">L'animazione viene riprodotta una volta e quindi si interrompe sull'ultimo frame.</span><span class="sxs-lookup"><span data-stu-id="c9b52-110">The animation plays once, and then it stops on the last frame.</span></span>

</dd> <dt>

<span data-ttu-id="c9b52-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**\_Pingpong D3DXPLAY**</span><span class="sxs-lookup"><span data-stu-id="c9b52-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY\_PINGPONG**</span></span>
</dt> <dd>

<span data-ttu-id="c9b52-112">L'animazione si alterna all'infinito tra la riproduzione in avanti e la riproduzione a ritroso.</span><span class="sxs-lookup"><span data-stu-id="c9b52-112">The animation alternates endlessly between playing forward and playing backward.</span></span>

</dd> <dt>

<span data-ttu-id="c9b52-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c9b52-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c9b52-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c9b52-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c9b52-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c9b52-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c9b52-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c9b52-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9b52-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9b52-117">Requirements</span></span>



| <span data-ttu-id="c9b52-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b52-118">Requirement</span></span> | <span data-ttu-id="c9b52-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c9b52-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b52-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9b52-120">Header</span></span><br/> | <dl> <span data-ttu-id="c9b52-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b52-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9b52-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9b52-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b52-123">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="c9b52-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




