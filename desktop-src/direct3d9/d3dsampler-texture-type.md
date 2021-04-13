---
description: Definisce i tipi di trama del campionatore per i vertex shader.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Enumerazione D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401930"
---
# <a name="d3dsampler_texture_type-enumeration"></a><span data-ttu-id="7c200-103">Enumerazione del tipo di \_ trama D3DSAMPLER \_</span><span class="sxs-lookup"><span data-stu-id="7c200-103">D3DSAMPLER\_TEXTURE\_TYPE enumeration</span></span>

<span data-ttu-id="7c200-104">Definisce i tipi di trama del campionatore per i vertex shader.</span><span class="sxs-lookup"><span data-stu-id="7c200-104">Defines the sampler texture types for vertex shaders.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c200-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c200-105">Syntax</span></span>


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="7c200-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="7c200-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7c200-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="7c200-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="7c200-108">Valore non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="7c200-108">Uninitialized value.</span></span> <span data-ttu-id="7c200-109">Il valore di questo elemento è 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="7c200-109">The value of this element is 0 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="7c200-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**</span><span class="sxs-lookup"><span data-stu-id="7c200-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT\_2D**</span></span>
</dt> <dd>

<span data-ttu-id="7c200-111">Dichiarazione di una trama 2D.</span><span class="sxs-lookup"><span data-stu-id="7c200-111">Declaring a 2D texture.</span></span> <span data-ttu-id="7c200-112">Il valore di questo elemento è 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="7c200-112">The value of this element is 2 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="7c200-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Cubo D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="7c200-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT\_CUBE**</span></span>
</dt> <dd>

<span data-ttu-id="7c200-114">Dichiarazione di una trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="7c200-114">Declaring a cube texture.</span></span> <span data-ttu-id="7c200-115">Il valore di questo elemento è 3 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="7c200-115">The value of this element is 3 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="7c200-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Volume D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="7c200-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="7c200-117">Dichiarazione di una trama del volume.</span><span class="sxs-lookup"><span data-stu-id="7c200-117">Declaring a volume texture.</span></span> <span data-ttu-id="7c200-118">Il valore di questo elemento è 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="7c200-118">The value of this element is 4 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="7c200-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7c200-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7c200-120">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7c200-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7c200-121">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7c200-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7c200-122">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7c200-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c200-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c200-123">Requirements</span></span>



| <span data-ttu-id="7c200-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c200-124">Requirement</span></span> | <span data-ttu-id="7c200-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7c200-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c200-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c200-126">Header</span></span><br/> | <dl> <span data-ttu-id="7c200-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c200-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c200-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c200-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c200-129">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="7c200-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




