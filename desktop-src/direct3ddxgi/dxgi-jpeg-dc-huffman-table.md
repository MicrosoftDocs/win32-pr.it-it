---
description: Viene descritta una tabella di un DC Huffman.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: Struttura DXGI_JPEG_DC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234991"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a><span data-ttu-id="30c8b-103">\_Struttura della tabella DXGI JPEG \_ DC \_ Huffman \_</span><span class="sxs-lookup"><span data-stu-id="30c8b-103">DXGI\_JPEG\_DC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="30c8b-104">Viene descritta una tabella di un DC Huffman.</span><span class="sxs-lookup"><span data-stu-id="30c8b-104">Describes a JPEG DC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c8b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30c8b-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="30c8b-106">Members</span><span class="sxs-lookup"><span data-stu-id="30c8b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="30c8b-107">**Codecounts**</span><span class="sxs-lookup"><span data-stu-id="30c8b-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="30c8b-108">Numero di codici per ogni lunghezza del codice.</span><span class="sxs-lookup"><span data-stu-id="30c8b-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="30c8b-109">**Codevalues**</span><span class="sxs-lookup"><span data-stu-id="30c8b-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="30c8b-110">Valori del codice del Huffman, in ordine di aumento della lunghezza del codice.</span><span class="sxs-lookup"><span data-stu-id="30c8b-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30c8b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30c8b-111">Requirements</span></span>



| <span data-ttu-id="30c8b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="30c8b-112">Requirement</span></span> | <span data-ttu-id="30c8b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="30c8b-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30c8b-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30c8b-114">Header</span></span><br/> | <dl> <span data-ttu-id="30c8b-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c8b-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30c8b-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30c8b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c8b-117">Strutture DXGI</span><span class="sxs-lookup"><span data-stu-id="30c8b-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




