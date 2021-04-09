---
description: Definisce le costanti che descrivono le modalità di indirizzamento della trama supportate.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Enumerazione D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058594"
---
# <a name="d3dtextureaddress-enumeration"></a><span data-ttu-id="bdc98-103">Enumerazione D3DTEXTUREADDRESS</span><span class="sxs-lookup"><span data-stu-id="bdc98-103">D3DTEXTUREADDRESS enumeration</span></span>

<span data-ttu-id="bdc98-104">Definisce le costanti che descrivono le modalità di indirizzamento della trama supportate.</span><span class="sxs-lookup"><span data-stu-id="bdc98-104">Defines constants that describe the supported texture-addressing modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc98-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdc98-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a><span data-ttu-id="bdc98-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="bdc98-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bdc98-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS a \_ capo**</span><span class="sxs-lookup"><span data-stu-id="bdc98-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS\_WRAP**</span></span>
</dt> <dd>

<span data-ttu-id="bdc98-108">Affiancare la trama a ogni giunzione di interi.</span><span class="sxs-lookup"><span data-stu-id="bdc98-108">Tile the texture at every integer junction.</span></span> <span data-ttu-id="bdc98-109">Ad esempio, per i valori compresi tra 0 e 3, la trama viene ripetuta tre volte. Nessun mirroring eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdc98-109">For example, for u values between 0 and 3, the texture is repeated three times; no mirroring is performed.</span></span>

</dd> <dt>

<span data-ttu-id="bdc98-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**\_Mirror D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="bdc98-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="bdc98-111">Simile a D3DTADDRESS \_ wrap, ad eccezione del fatto che la trama viene capovolta a ogni giunzione di interi.</span><span class="sxs-lookup"><span data-stu-id="bdc98-111">Similar to D3DTADDRESS\_WRAP, except that the texture is flipped at every integer junction.</span></span> <span data-ttu-id="bdc98-112">per i valori compresi tra 0 e 1, ad esempio, la trama viene risolta normalmente; tra 1 e 2 la trama viene capovolta (con mirroring); da 2 a 3, la trama è di nuovo normale; E così via.</span><span class="sxs-lookup"><span data-stu-id="bdc98-112">For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.</span></span>

</dd> <dt>

<span data-ttu-id="bdc98-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**\_Clamp D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="bdc98-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS\_CLAMP**</span></span>
</dt> <dd>

<span data-ttu-id="bdc98-114">Le coordinate di trama non comprese nell'intervallo \[ 0,0, 1,0 \] sono impostate rispettivamente sul colore della trama a 0,0 o 1,0.</span><span class="sxs-lookup"><span data-stu-id="bdc98-114">Texture coordinates outside the range \[0.0, 1.0\] are set to the texture color at 0.0 or 1.0, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="bdc98-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**\_Bordo D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="bdc98-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS\_BORDER**</span></span>
</dt> <dd>

<span data-ttu-id="bdc98-116">Le coordinate di trama non comprese nell'intervallo \[ 0,0, 1,0 \] sono impostate sul colore del bordo.</span><span class="sxs-lookup"><span data-stu-id="bdc98-116">Texture coordinates outside the range \[0.0, 1.0\] are set to the border color.</span></span>

</dd> <dt>

<span data-ttu-id="bdc98-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**\_MIRRORONCE D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="bdc98-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS\_MIRRORONCE**</span></span>
</dt> <dd>

<span data-ttu-id="bdc98-118">Simile a D3DTADDRESS \_ mirror e D3DTADDRESS \_ Clamp.</span><span class="sxs-lookup"><span data-stu-id="bdc98-118">Similar to D3DTADDRESS\_MIRROR and D3DTADDRESS\_CLAMP.</span></span> <span data-ttu-id="bdc98-119">Accetta il valore assoluto della coordinata di trama (pertanto, il mirroring circa 0) e quindi il morsetto al valore massimo.</span><span class="sxs-lookup"><span data-stu-id="bdc98-119">Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.</span></span> <span data-ttu-id="bdc98-120">L'utilizzo più comune è per le trame del volume, in cui il supporto per la \_ modalità di indirizzamento della trama D3DTADDRESS MIRRORONCE completa non è necessario, ma i dati sono simmetrici intorno a un asse.</span><span class="sxs-lookup"><span data-stu-id="bdc98-120">The most common usage is for volume textures, where support for the full D3DTADDRESS\_MIRRORONCE texture-addressing mode is not necessary, but the data is symmetric around the one axis.</span></span>

</dd> <dt>

<span data-ttu-id="bdc98-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bdc98-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="bdc98-122">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="bdc98-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="bdc98-123">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="bdc98-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="bdc98-124">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="bdc98-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdc98-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdc98-125">Requirements</span></span>



| <span data-ttu-id="bdc98-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc98-126">Requirement</span></span> | <span data-ttu-id="bdc98-127">Valore</span><span class="sxs-lookup"><span data-stu-id="bdc98-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc98-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdc98-128">Header</span></span><br/> | <dl> <span data-ttu-id="bdc98-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc98-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc98-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdc98-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc98-131">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="bdc98-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="bdc98-132">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="bdc98-132">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
