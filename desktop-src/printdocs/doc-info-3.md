---
description: La \_ struttura doc info \_ 3 descrive un documento che verrà stampato.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Struttura DOC_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311547"
---
# <a name="doc_info_3-structure"></a><span data-ttu-id="9b725-103">\_Struttura doc info \_ 3</span><span class="sxs-lookup"><span data-stu-id="9b725-103">DOC\_INFO\_3 structure</span></span>

<span data-ttu-id="9b725-104">La struttura **doc \_ info \_ 3** descrive un documento che verrà stampato.</span><span class="sxs-lookup"><span data-stu-id="9b725-104">The **DOC\_INFO\_3** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b725-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b725-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a><span data-ttu-id="9b725-106">Members</span><span class="sxs-lookup"><span data-stu-id="9b725-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9b725-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="9b725-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="9b725-108">Puntatore a una stringa con terminazione null che specifica il nome del documento.</span><span class="sxs-lookup"><span data-stu-id="9b725-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="9b725-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="9b725-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="9b725-110">Puntatore a una stringa con terminazione null che specifica il nome di un file di output.</span><span class="sxs-lookup"><span data-stu-id="9b725-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="9b725-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="9b725-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="9b725-112">Puntatore a una stringa con terminazione null che identifica il tipo di dati utilizzati per registrare il documento.</span><span class="sxs-lookup"><span data-stu-id="9b725-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="9b725-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="9b725-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9b725-114">Bandiere.</span><span class="sxs-lookup"><span data-stu-id="9b725-114">Flags.</span></span> <span data-ttu-id="9b725-115">Attualmente può essere **null** o quanto segue.</span><span class="sxs-lookup"><span data-stu-id="9b725-115">Currently, it can be **NULL** or the following.</span></span>



| <span data-ttu-id="9b725-116">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="9b725-116">Flag</span></span>                 | <span data-ttu-id="9b725-117">Significato</span><span class="sxs-lookup"><span data-stu-id="9b725-117">Meaning</span></span>                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b725-118">\_scrittura di MEMORYMAP \_</span><span class="sxs-lookup"><span data-stu-id="9b725-118">DI\_MEMORYMAP\_WRITE</span></span> | <span data-ttu-id="9b725-119">Fa in modo che [**StartDocPrinter**](startdocprinter.md) non usi [**AddJob**](addjob.md) e [**ScheduleJob**](schedulejob.md) per la stampa locale.</span><span class="sxs-lookup"><span data-stu-id="9b725-119">Causes [**StartDocPrinter**](startdocprinter.md) to not use [**AddJob**](addjob.md) and [**ScheduleJob**](schedulejob.md) for local printing.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b725-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b725-120">Remarks</span></span>

<span data-ttu-id="9b725-121">L' \_ impostazione di scrittura di MEMORYMAP \_ in **doc \_ info \_ 3** è un'ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="9b725-121">The DI\_MEMORYMAP\_WRITE setting in **DOC\_INFO\_3** is an optimization.</span></span> <span data-ttu-id="9b725-122">Questo consente a GDI di mappare i file di spooling nell'applicazione e velocizzare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="9b725-122">This allows GDI to map spool files in the application and speed up the recording.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b725-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b725-123">Requirements</span></span>



| <span data-ttu-id="9b725-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b725-124">Requirement</span></span> | <span data-ttu-id="9b725-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9b725-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b725-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b725-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9b725-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9b725-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9b725-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b725-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9b725-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9b725-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9b725-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b725-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b725-131"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b725-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9b725-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9b725-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9b725-133">**\_ \_ Info doc \_ 3W** (Unicode) e **\_ informazioni del documento \_ \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9b725-133">**\_DOC\_INFO\_3W** (Unicode) and **\_DOC\_INFO\_3A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="9b725-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b725-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b725-135">Stampa</span><span class="sxs-lookup"><span data-stu-id="9b725-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9b725-136">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="9b725-136">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9b725-137">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="9b725-137">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="9b725-138">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="9b725-138">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="9b725-139">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="9b725-139">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




