---
description: Descrive una tabella di Huffman AC JPEG.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: Struttura DXGI_JPEG_AC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322520"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a><span data-ttu-id="8445d-103">\_Struttura della \_ \_ tabella Huffman AC DXGI JPEG \_</span><span class="sxs-lookup"><span data-stu-id="8445d-103">DXGI\_JPEG\_AC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="8445d-104">Descrive una tabella di Huffman AC JPEG.</span><span class="sxs-lookup"><span data-stu-id="8445d-104">Describes a JPEG AC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="8445d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8445d-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="8445d-106">Members</span><span class="sxs-lookup"><span data-stu-id="8445d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8445d-107">**Codecounts**</span><span class="sxs-lookup"><span data-stu-id="8445d-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="8445d-108">Numero di codici per ogni lunghezza del codice.</span><span class="sxs-lookup"><span data-stu-id="8445d-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="8445d-109">**Codevalues**</span><span class="sxs-lookup"><span data-stu-id="8445d-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="8445d-110">Valori del codice del Huffman, in ordine di aumento della lunghezza del codice.</span><span class="sxs-lookup"><span data-stu-id="8445d-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8445d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8445d-111">Requirements</span></span>



| <span data-ttu-id="8445d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8445d-112">Requirement</span></span> | <span data-ttu-id="8445d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8445d-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8445d-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8445d-114">Header</span></span><br/> | <dl> <span data-ttu-id="8445d-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="8445d-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8445d-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8445d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8445d-117">Strutture DXGI</span><span class="sxs-lookup"><span data-stu-id="8445d-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




