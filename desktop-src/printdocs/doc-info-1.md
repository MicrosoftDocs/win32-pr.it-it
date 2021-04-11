---
description: La \_ struttura doc info \_ 1 descrive un documento che verrà stampato.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Struttura DOC_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227354"
---
# <a name="doc_info_1-structure"></a><span data-ttu-id="e9f67-103">Struttura del documento \_ info \_ 1</span><span class="sxs-lookup"><span data-stu-id="e9f67-103">DOC\_INFO\_1 structure</span></span>

<span data-ttu-id="e9f67-104">La struttura **doc \_ info \_ 1** descrive un documento che verrà stampato.</span><span class="sxs-lookup"><span data-stu-id="e9f67-104">The **DOC\_INFO\_1** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f67-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f67-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a><span data-ttu-id="e9f67-106">Members</span><span class="sxs-lookup"><span data-stu-id="e9f67-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9f67-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="e9f67-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-108">Puntatore a una stringa con terminazione null che specifica il nome del documento.</span><span class="sxs-lookup"><span data-stu-id="e9f67-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="e9f67-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-110">Puntatore a una stringa con terminazione null che specifica il nome di un file di output.</span><span class="sxs-lookup"><span data-stu-id="e9f67-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span> <span data-ttu-id="e9f67-111">Per stampare su una stampante, impostarla su **null**.</span><span class="sxs-lookup"><span data-stu-id="e9f67-111">To print to a printer, set this to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-112">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="e9f67-112">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-113">Puntatore a una stringa con terminazione null che identifica il tipo di dati utilizzati per registrare il documento.</span><span class="sxs-lookup"><span data-stu-id="e9f67-113">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9f67-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f67-114">Requirements</span></span>



| <span data-ttu-id="e9f67-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f67-115">Requirement</span></span> | <span data-ttu-id="e9f67-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f67-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f67-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f67-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f67-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9f67-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e9f67-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f67-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f67-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9f67-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e9f67-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9f67-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f67-122"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9f67-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e9f67-123">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e9f67-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9f67-124">**\_ \_ Info doc \_ 1W** (Unicode) e **\_ doc \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e9f67-124">**\_DOC\_INFO\_1W** (Unicode) and **\_DOC\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="e9f67-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f67-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f67-126">Stampa</span><span class="sxs-lookup"><span data-stu-id="e9f67-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e9f67-127">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="e9f67-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e9f67-128">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="e9f67-128">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




