---
description: La \_ struttura PROVIDOR info \_ 2 aggiunge un provider di stampa all'elenco di ordini del provider di stampa.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Struttura PROVIDOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316417"
---
# <a name="providor_info_2-structure"></a><span data-ttu-id="16510-103">\_Struttura PROVIDOR info \_ 2</span><span class="sxs-lookup"><span data-stu-id="16510-103">PROVIDOR\_INFO\_2 structure</span></span>

<span data-ttu-id="16510-104">La struttura **PROVIDOR \_ info \_ 2** aggiunge un provider di stampa all'elenco di ordini del provider di stampa.</span><span class="sxs-lookup"><span data-stu-id="16510-104">The **PROVIDOR\_INFO\_2** structure appends a print provider to the print provider order list.</span></span>

## <a name="syntax"></a><span data-ttu-id="16510-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16510-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="16510-106">Members</span><span class="sxs-lookup"><span data-stu-id="16510-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="16510-107">**pOrder**</span><span class="sxs-lookup"><span data-stu-id="16510-107">**pOrder**</span></span>
</dt> <dd>

<span data-ttu-id="16510-108">Puntatore a una stringa con terminazione null che specifica il nome del provider di stampa.</span><span class="sxs-lookup"><span data-stu-id="16510-108">Pointer to a null-terminated string that specifies the name of the print provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16510-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="16510-109">Remarks</span></span>

<span data-ttu-id="16510-110">Questa struttura viene utilizzata quando si chiama [**AddPrintProvidor**](addprintprovidor.md), Level 2, per aggiungere il provider di stampa specificato alla fine dell'elenco di ordini del provider di stampa.</span><span class="sxs-lookup"><span data-stu-id="16510-110">This structure is used when calling [**AddPrintProvidor**](addprintprovidor.md), level 2, to add the specified print provider to the end of the print provider order list.</span></span> <span data-ttu-id="16510-111">Il provider viene utilizzato immediatamente per il routing se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="16510-111">The provider is immediately used for routing if the call succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="16510-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16510-112">Requirements</span></span>



| <span data-ttu-id="16510-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="16510-113">Requirement</span></span> | <span data-ttu-id="16510-114">Valore</span><span class="sxs-lookup"><span data-stu-id="16510-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16510-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16510-115">Minimum supported client</span></span><br/> | <span data-ttu-id="16510-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="16510-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="16510-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16510-117">Minimum supported server</span></span><br/> | <span data-ttu-id="16510-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="16510-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="16510-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16510-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="16510-120"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16510-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="16510-121">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="16510-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="16510-122">**\_ PROVIDOR \_ info \_ 2W** (Unicode) e **\_ PROVIDOR \_ info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="16510-122">**\_PROVIDOR\_INFO\_2W** (Unicode) and **\_PROVIDOR\_INFO\_2A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="16510-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16510-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16510-124">Stampa</span><span class="sxs-lookup"><span data-stu-id="16510-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="16510-125">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="16510-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="16510-126">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="16510-126">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




