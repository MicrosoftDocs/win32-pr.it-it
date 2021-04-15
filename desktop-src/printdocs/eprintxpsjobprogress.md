---
description: Specifica lo spooler attualmente in corso durante l'elaborazione di un processo di stampa XPS.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: Enumerazione EPrintXPSJobProgress (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2a09b55ed72a6276a1a9d224cc08e03546f887d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529544"
---
# <a name="eprintxpsjobprogress-enumeration"></a><span data-ttu-id="4e4c2-103">Enumerazione EPrintXPSJobProgress</span><span class="sxs-lookup"><span data-stu-id="4e4c2-103">EPrintXPSJobProgress enumeration</span></span>

<span data-ttu-id="4e4c2-104">Specifica lo spooler attualmente in corso durante l'elaborazione di un processo di stampa XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-104">Specifies what the spooler is currently doing as it processes an XPS print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e4c2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e4c2-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a><span data-ttu-id="4e4c2-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="4e4c2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4e4c2-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-108">Una sequenza di documenti sta per essere aggiunta al processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-108">A document sequence is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-110">È stata aggiunta una sequenza di documenti al processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-110">A document sequence has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-112">Un documento fisso sta per essere aggiunto al processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-112">A fixed document is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-114">Un documento fisso è stato aggiunto al processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-114">A fixed document has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-116">Una pagina sta per essere aggiunta al processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-116">A page is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-118">È stata aggiunta una pagina al processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-118">A page has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-120">Una risorsa è stata aggiunta al processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-120">A resource had been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-122">Al processo XPS è stato aggiunto un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-122">A font has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-124">Un'immagine è stata aggiunta al processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-124">An image has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c2-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span><span class="sxs-lookup"><span data-stu-id="4e4c2-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span></span>
</dt> <dd>

<span data-ttu-id="4e4c2-126">È stato eseguito il commit dei dati per il processo XPS.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-126">The data for the XPS job has been committed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e4c2-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e4c2-127">Remarks</span></span>

<span data-ttu-id="4e4c2-128">Questa enumerazione viene utilizzata principalmente come parametro per la funzione [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="4e4c2-128">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

<span data-ttu-id="4e4c2-129">Questi valori possono fare riferimento alla fase di spooling o di rendering di un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="4e4c2-129">These values can refer to either the spooling or the rendering phase of a print job.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e4c2-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e4c2-130">Requirements</span></span>



| <span data-ttu-id="4e4c2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e4c2-131">Requirement</span></span> | <span data-ttu-id="4e4c2-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4e4c2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4c2-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e4c2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4e4c2-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e4c2-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4e4c2-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e4c2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4e4c2-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e4c2-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e4c2-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e4c2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e4c2-138"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e4c2-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




