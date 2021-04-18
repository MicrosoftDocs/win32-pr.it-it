---
description: La \_ struttura PRINTPROCESSOR info \_ 1 specifica il nome di un processore di stampa installato.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: Struttura PRINTPROCESSOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315980"
---
# <a name="printprocessor_info_1-structure"></a><span data-ttu-id="bf86d-103">\_Struttura PRINTPROCESSOR info \_ 1</span><span class="sxs-lookup"><span data-stu-id="bf86d-103">PRINTPROCESSOR\_INFO\_1 structure</span></span>

<span data-ttu-id="bf86d-104">La struttura **PRINTPROCESSOR \_ info \_ 1** specifica il nome di un processore di stampa installato.</span><span class="sxs-lookup"><span data-stu-id="bf86d-104">The **PRINTPROCESSOR\_INFO\_1** structure specifies the name of an installed print processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf86d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf86d-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="bf86d-106">Members</span><span class="sxs-lookup"><span data-stu-id="bf86d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf86d-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="bf86d-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="bf86d-108">Puntatore a una stringa con terminazione null che specifica il nome di un processore di stampa installato.</span><span class="sxs-lookup"><span data-stu-id="bf86d-108">Pointer to a null-terminated string that specifies the name of an installed print processor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf86d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf86d-109">Requirements</span></span>



| <span data-ttu-id="bf86d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf86d-110">Requirement</span></span> | <span data-ttu-id="bf86d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="bf86d-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf86d-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf86d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bf86d-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf86d-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bf86d-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf86d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bf86d-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf86d-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bf86d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf86d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf86d-117"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf86d-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bf86d-118">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bf86d-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bf86d-119">**\_ PRINTPROCESSOR \_ info \_ 1W** (Unicode) e **\_ PRINTPROCESSOR \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bf86d-119">**\_PRINTPROCESSOR\_INFO\_1W** (Unicode) and **\_PRINTPROCESSOR\_INFO\_1A** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bf86d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf86d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf86d-121">Stampa</span><span class="sxs-lookup"><span data-stu-id="bf86d-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bf86d-122">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="bf86d-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="bf86d-123">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="bf86d-123">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

 




