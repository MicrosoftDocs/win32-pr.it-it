---
description: ICEM07 verifica che l'ordine dei file nella tabella di sequenza corrisponda all'ordine dei file in MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882410"
---
# <a name="icem07"></a><span data-ttu-id="87c80-103">ICEM07</span><span class="sxs-lookup"><span data-stu-id="87c80-103">ICEM07</span></span>

<span data-ttu-id="87c80-104">ICEM07 verifica che l'ordine dei file nella tabella di sequenza corrisponda all'ordine dei file in [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="87c80-104">ICEM07 verifies that the order of files in the sequence table matches the order of files in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span>

<span data-ttu-id="87c80-105">I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87c80-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="87c80-106">Risultato</span><span class="sxs-lookup"><span data-stu-id="87c80-106">Result</span></span>

<span data-ttu-id="87c80-107">ICEM07 Invia un errore se l'ordine dei file nella tabella file non corrisponde all'ordine nel file CAB.</span><span class="sxs-lookup"><span data-stu-id="87c80-107">ICEM07 posts an error if the order of files in the File table does not match the order in the cabinet file.</span></span>

## <a name="example"></a><span data-ttu-id="87c80-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="87c80-108">Example</span></span>

<span data-ttu-id="87c80-109">IC0M07 invia il messaggio di errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="87c80-109">IC0M07 would post the following error message for the example shown.</span></span>

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[<span data-ttu-id="87c80-110">Tabella file</span><span class="sxs-lookup"><span data-stu-id="87c80-110">File Table</span></span>](file-table.md)



| <span data-ttu-id="87c80-111">File</span><span class="sxs-lookup"><span data-stu-id="87c80-111">File</span></span>          | <span data-ttu-id="87c80-112">Sequenza</span><span class="sxs-lookup"><span data-stu-id="87c80-112">Sequence</span></span> |
|---------------|----------|
| <span data-ttu-id="87c80-113">Filea. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="87c80-113">FileA.*GUID1*</span></span> | <span data-ttu-id="87c80-114">1</span><span class="sxs-lookup"><span data-stu-id="87c80-114">1</span></span>        |
| <span data-ttu-id="87c80-115">FileB. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="87c80-115">FileB.*GUID1*</span></span> | <span data-ttu-id="87c80-116">8</span><span class="sxs-lookup"><span data-stu-id="87c80-116">8</span></span>        |
| <span data-ttu-id="87c80-117">FileC. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="87c80-117">FileC.*GUID1*</span></span> | <span data-ttu-id="87c80-118">52</span><span class="sxs-lookup"><span data-stu-id="87c80-118">52</span></span>       |



 

<span data-ttu-id="87c80-119">Incorporato [MergeModule.CABinet](mergemodule-cabinet.md)</span><span class="sxs-lookup"><span data-stu-id="87c80-119">Embedded [MergeModule.CABinet](mergemodule-cabinet.md)</span></span>



| <span data-ttu-id="87c80-120">File</span><span class="sxs-lookup"><span data-stu-id="87c80-120">File</span></span>          |
|---------------|
| <span data-ttu-id="87c80-121">Filea. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="87c80-121">FileA.*GUID1*</span></span> |
| <span data-ttu-id="87c80-122">FileC. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="87c80-122">FileC.*GUID1*</span></span> |
| <span data-ttu-id="87c80-123">Campo. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="87c80-123">FileD.*GUID1*</span></span> |
| <span data-ttu-id="87c80-124">FileB. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="87c80-124">FileB.*GUID1*</span></span> |



 

<span data-ttu-id="87c80-125">Sebbene i numeri di sequenza di file nella tabella file non debbano essere consecutivi e i file aggiuntivi possano esistere nel file CAB, la sequenza relativa di tutti i file nella tabella file deve corrispondere all'ordine in [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="87c80-125">Although the file sequence numbers in the file table do not have to be consecutive, and extra files can exist in the cabinet file, the relative sequence of all files in the File table must match the order in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span> <span data-ttu-id="87c80-126">Per correggere l'errore, modificare il numero di sequenza di FileB in modo che arrivi dopo FileC in modo che corrisponda all'ordine del file nel file CAB oppure ricompilare il file CAB con i file nell'ordine corretto.</span><span class="sxs-lookup"><span data-stu-id="87c80-126">To fix this error, change the sequence number of FileB to come after FileC to match the file order in the CAB, or rebuild the CAB with the files in the correct order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87c80-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87c80-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87c80-128">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="87c80-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



