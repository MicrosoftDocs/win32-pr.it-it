---
description: La \_ struttura PROVIDOR info \_ 1 identifica un provider di stampa.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: Struttura PROVIDOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347486"
---
# <a name="providor_info_1-structure"></a><span data-ttu-id="0602b-103">\_Struttura PROVIDOR info \_ 1</span><span class="sxs-lookup"><span data-stu-id="0602b-103">PROVIDOR\_INFO\_1 structure</span></span>

<span data-ttu-id="0602b-104">La struttura **PROVIDOR \_ info \_ 1** identifica un provider di stampa.</span><span class="sxs-lookup"><span data-stu-id="0602b-104">The **PROVIDOR\_INFO\_1** structure identifies a print provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="0602b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0602b-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="0602b-106">Members</span><span class="sxs-lookup"><span data-stu-id="0602b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0602b-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="0602b-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="0602b-108">Puntatore a una stringa con terminazione null che rappresenta il nome del provider di stampa.</span><span class="sxs-lookup"><span data-stu-id="0602b-108">Pointer to a null-terminated string that is the name of the print provider.</span></span>

</dd> <dt>

<span data-ttu-id="0602b-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="0602b-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="0602b-110">Puntatore a una stringa di ambiente con terminazione null che specifica l'ambiente in cui è progettata la libreria di collegamento dinamico (DLL) del provider.</span><span class="sxs-lookup"><span data-stu-id="0602b-110">Pointer to a null-terminated environment string specifying the environment the provider dynamic-link library (DLL) is designed to run in.</span></span>

</dd> <dt>

<span data-ttu-id="0602b-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="0602b-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="0602b-112">Puntatore a una stringa con terminazione null che rappresenta il nome del provider. dll.</span><span class="sxs-lookup"><span data-stu-id="0602b-112">Pointer to a null-terminated string that is the name of the provider .dll.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0602b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0602b-113">Requirements</span></span>



| <span data-ttu-id="0602b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0602b-114">Requirement</span></span> | <span data-ttu-id="0602b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0602b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0602b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0602b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0602b-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0602b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0602b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0602b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0602b-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0602b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0602b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0602b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0602b-121"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0602b-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0602b-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0602b-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0602b-123">**\_ PROVIDOR \_ info \_ 1W** (Unicode) e **\_ PROVIDOR \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0602b-123">**\_PROVIDOR\_INFO\_1W** (Unicode) and **\_PROVIDOR\_INFO\_1A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="0602b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0602b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0602b-125">Stampa</span><span class="sxs-lookup"><span data-stu-id="0602b-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0602b-126">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="0602b-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="0602b-127">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="0602b-127">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




