---
description: La \_ struttura doc info \_ 2 descrive un documento che verrà stampato.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Struttura DOC_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316426"
---
# <a name="doc_info_2-structure"></a><span data-ttu-id="0e34a-103">\_Struttura doc info \_ 2</span><span class="sxs-lookup"><span data-stu-id="0e34a-103">DOC\_INFO\_2 structure</span></span>

<span data-ttu-id="0e34a-104">La struttura **doc \_ info \_ 2** descrive un documento che verrà stampato.</span><span class="sxs-lookup"><span data-stu-id="0e34a-104">The **DOC\_INFO\_2** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e34a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e34a-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a><span data-ttu-id="0e34a-106">Members</span><span class="sxs-lookup"><span data-stu-id="0e34a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0e34a-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="0e34a-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="0e34a-108">Puntatore a una stringa con terminazione null che specifica il nome del documento.</span><span class="sxs-lookup"><span data-stu-id="0e34a-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="0e34a-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="0e34a-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="0e34a-110">Puntatore a una stringa con terminazione null che specifica il nome di un file di output.</span><span class="sxs-lookup"><span data-stu-id="0e34a-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="0e34a-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="0e34a-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="0e34a-112">Puntatore a una stringa con terminazione null che identifica il tipo di dati utilizzati per registrare il documento.</span><span class="sxs-lookup"><span data-stu-id="0e34a-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="0e34a-113">**dwMode**</span><span class="sxs-lookup"><span data-stu-id="0e34a-113">**dwMode**</span></span>
</dt> <dd>

<span data-ttu-id="0e34a-114">Informa lo spooler di stampa della natura dei dati da seguire.</span><span class="sxs-lookup"><span data-stu-id="0e34a-114">Informs the print spooler of the nature of the data to follow.</span></span> <span data-ttu-id="0e34a-115">Se questo valore è zero, lo spooler di stampa considera i dati inviati dalle chiamate successive a [**WritePrinter**](writeprinter.md) come processo di stampa normale (indipendentemente dal fatto che venga eseguito lo spooling a seconda della proprietà della stampante).</span><span class="sxs-lookup"><span data-stu-id="0e34a-115">If this value is zero, the print spooler treats the data sent by subsequent calls to [**WritePrinter**](writeprinter.md) as a normal print job (whether or not it is spooled depends on the printer property).</span></span> <span data-ttu-id="0e34a-116">Se questo valore è DI \_ canale di, viene aperto solo un canale di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="0e34a-116">If this value is DI\_CHANNEL, only a communications channel is opened.</span></span> <span data-ttu-id="0e34a-117">In questo caso, i dati passati alle chiamate successive a **WritePrinter** vengono inviati alla stampante o alle chiamate successive a [**ReadPrinter**](readprinter.md) per recuperare i dati dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="0e34a-117">In this case, the data passed into subsequent calls to **WritePrinter** is sent to the printer or subsequent calls to [**ReadPrinter**](readprinter.md) retrieve data from the printer.</span></span> <span data-ttu-id="0e34a-118">Questa modalità rimane valida fino a quando non viene chiamato [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .</span><span class="sxs-lookup"><span data-stu-id="0e34a-118">This mode remains effective until [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) is called.</span></span>

</dd> <dt>

<span data-ttu-id="0e34a-119">**JobId**</span><span class="sxs-lookup"><span data-stu-id="0e34a-119">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="0e34a-120">Riservato per uso interno; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0e34a-120">Reserved for internal use; should be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e34a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e34a-121">Requirements</span></span>



| <span data-ttu-id="0e34a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e34a-122">Requirement</span></span> | <span data-ttu-id="0e34a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0e34a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e34a-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e34a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0e34a-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e34a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0e34a-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e34a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0e34a-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e34a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0e34a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e34a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e34a-129"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e34a-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0e34a-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0e34a-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e34a-131">**\_ \_ Info doc \_ 2W** (Unicode) e **\_ doc \_ info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0e34a-131">**\_DOC\_INFO\_2W** (Unicode) and **\_DOC\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="0e34a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e34a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e34a-133">Stampa</span><span class="sxs-lookup"><span data-stu-id="0e34a-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0e34a-134">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="0e34a-134">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="0e34a-135">**EndDoc**</span><span class="sxs-lookup"><span data-stu-id="0e34a-135">**EndDoc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[<span data-ttu-id="0e34a-136">**ReadPrinter**</span><span class="sxs-lookup"><span data-stu-id="0e34a-136">**ReadPrinter**</span></span>](readprinter.md)
</dt> <dt>

[<span data-ttu-id="0e34a-137">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="0e34a-137">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="0e34a-138">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="0e34a-138">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




