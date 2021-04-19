---
description: Descrive una tabella di quantizzazione JPEG.
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: Struttura DXGI_JPEG_QUANTIZATION_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322517"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a><span data-ttu-id="88573-103">\_Struttura della \_ tabella di quantizzazione JPEG DXGI \_</span><span class="sxs-lookup"><span data-stu-id="88573-103">DXGI\_JPEG\_QUANTIZATION\_TABLE structure</span></span>

<span data-ttu-id="88573-104">Descrive una tabella di quantizzazione JPEG.</span><span class="sxs-lookup"><span data-stu-id="88573-104">Describes a JPEG quantization table.</span></span>

## <a name="syntax"></a><span data-ttu-id="88573-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88573-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a><span data-ttu-id="88573-106">Members</span><span class="sxs-lookup"><span data-stu-id="88573-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="88573-107">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="88573-107">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="88573-108">Matrice di byte contenente gli elementi della tabella di quantizzazione.</span><span class="sxs-lookup"><span data-stu-id="88573-108">An array of bytes containing the elements of the quantization table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88573-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88573-109">Requirements</span></span>



| <span data-ttu-id="88573-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="88573-110">Requirement</span></span> | <span data-ttu-id="88573-111">Valore</span><span class="sxs-lookup"><span data-stu-id="88573-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88573-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88573-112">Header</span></span><br/> | <dl> <span data-ttu-id="88573-113"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="88573-113"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88573-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88573-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88573-115">Strutture DXGI</span><span class="sxs-lookup"><span data-stu-id="88573-115">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




