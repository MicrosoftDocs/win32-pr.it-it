---
description: ICE32 verifica che le chiavi e le chiavi esterne nel file con estensione msi abbiano lo stesso tipo di definizione delle dimensioni e della colonna.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314223"
---
# <a name="ice32"></a><span data-ttu-id="daf76-103">ICE32</span><span class="sxs-lookup"><span data-stu-id="daf76-103">ICE32</span></span>

<span data-ttu-id="daf76-104">ICE32 verifica che le chiavi e le chiavi esterne nel file con estensione msi abbiano lo stesso tipo di definizione delle dimensioni e della colonna.</span><span class="sxs-lookup"><span data-stu-id="daf76-104">ICE32 validates that keys and foreign keys in the .msi file are of the same size and column definition types.</span></span> <span data-ttu-id="daf76-105">Questa azione personalizzata ICE esegue il confronto usando la [ \_ tabella di convalida](-validation-table.md) e usando i tipi di definizione restituiti da [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span><span class="sxs-lookup"><span data-stu-id="daf76-105">This ICE custom action makes the comparison using the [\_Validation table](-validation-table.md) and using the definition types that are returned by [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span></span> <span data-ttu-id="daf76-106">Per altre informazioni, vedere [formato della definizione di colonna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="daf76-106">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

## <a name="result"></a><span data-ttu-id="daf76-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="daf76-107">Result</span></span>

<span data-ttu-id="daf76-108">ICE32 Invia errori se il file con estensione msi contiene chiavi esterne alle chiavi di un tipo di dati di colonna o di colonna diverso.</span><span class="sxs-lookup"><span data-stu-id="daf76-108">ICE32 posts errors if the .msi file contains any foreign keys to keys of a different column length or column data type.</span></span>

## <a name="example"></a><span data-ttu-id="daf76-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="daf76-109">Example</span></span>

<span data-ttu-id="daf76-110">ICE32 invia due errori per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="daf76-110">ICE32 posts two errors for the example shown:</span></span>

-   <span data-ttu-id="daf76-111">È stata definita una chiave esterna e una chiave di dimensioni diverse.</span><span class="sxs-lookup"><span data-stu-id="daf76-111">There is a foreign key and key defined that differ in size.</span></span>
-   <span data-ttu-id="daf76-112">È stata definita una chiave esterna e una chiave che differiscono nel tipo di definizione.</span><span class="sxs-lookup"><span data-stu-id="daf76-112">There is a foreign key and key defined that differ in their definition type.</span></span>

<span data-ttu-id="daf76-113">[ \_ Tabella di convalida](-validation-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="daf76-113">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="daf76-114">Tabella</span><span class="sxs-lookup"><span data-stu-id="daf76-114">Table</span></span> | <span data-ttu-id="daf76-115">Colonna</span><span class="sxs-lookup"><span data-stu-id="daf76-115">Column</span></span>  | <span data-ttu-id="daf76-116">KeyTable</span><span class="sxs-lookup"><span data-stu-id="daf76-116">KeyTable</span></span> | <span data-ttu-id="daf76-117">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="daf76-117">KeyColumn</span></span> |
|-------|---------|----------|-----------|
| <span data-ttu-id="daf76-118">File</span><span class="sxs-lookup"><span data-stu-id="daf76-118">File</span></span>  | <span data-ttu-id="daf76-119">Version</span><span class="sxs-lookup"><span data-stu-id="daf76-119">Version</span></span> | <span data-ttu-id="daf76-120">File</span><span class="sxs-lookup"><span data-stu-id="daf76-120">File</span></span>     | <span data-ttu-id="daf76-121">1</span><span class="sxs-lookup"><span data-stu-id="daf76-121">1</span></span>         |
| <span data-ttu-id="daf76-122">Flap</span><span class="sxs-lookup"><span data-stu-id="daf76-122">Flap</span></span>  | <span data-ttu-id="daf76-123">Colonna8</span><span class="sxs-lookup"><span data-stu-id="daf76-123">Column8</span></span> | <span data-ttu-id="daf76-124">Flap</span><span class="sxs-lookup"><span data-stu-id="daf76-124">Flap</span></span>     | <span data-ttu-id="daf76-125">1</span><span class="sxs-lookup"><span data-stu-id="daf76-125">1</span></span>         |



 

<span data-ttu-id="daf76-126">Definizioni di colonna (parziali)</span><span class="sxs-lookup"><span data-stu-id="daf76-126">Column Definitions (partial)</span></span>



| <span data-ttu-id="daf76-127">Tabella</span><span class="sxs-lookup"><span data-stu-id="daf76-127">Table</span></span> | <span data-ttu-id="daf76-128">Colonna</span><span class="sxs-lookup"><span data-stu-id="daf76-128">Column</span></span>  | <span data-ttu-id="daf76-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="daf76-129">Type</span></span> | <span data-ttu-id="daf76-130">Dimensione</span><span class="sxs-lookup"><span data-stu-id="daf76-130">Size</span></span> |
|-------|---------|------|------|
| <span data-ttu-id="daf76-131">File</span><span class="sxs-lookup"><span data-stu-id="daf76-131">File</span></span>  | <span data-ttu-id="daf76-132">File</span><span class="sxs-lookup"><span data-stu-id="daf76-132">File</span></span>    | <span data-ttu-id="daf76-133">s</span><span class="sxs-lookup"><span data-stu-id="daf76-133">s</span></span>    | <span data-ttu-id="daf76-134">72</span><span class="sxs-lookup"><span data-stu-id="daf76-134">72</span></span>   |
| <span data-ttu-id="daf76-135">File</span><span class="sxs-lookup"><span data-stu-id="daf76-135">File</span></span>  | <span data-ttu-id="daf76-136">Versione</span><span class="sxs-lookup"><span data-stu-id="daf76-136">Version</span></span> | <span data-ttu-id="daf76-137">S</span><span class="sxs-lookup"><span data-stu-id="daf76-137">S</span></span>    | <span data-ttu-id="daf76-138">32</span><span class="sxs-lookup"><span data-stu-id="daf76-138">32</span></span>   |
| <span data-ttu-id="daf76-139">Flap</span><span class="sxs-lookup"><span data-stu-id="daf76-139">Flap</span></span>  | <span data-ttu-id="daf76-140">Colonna 1</span><span class="sxs-lookup"><span data-stu-id="daf76-140">Column1</span></span> | <span data-ttu-id="daf76-141">i</span><span class="sxs-lookup"><span data-stu-id="daf76-141">i</span></span>    | <span data-ttu-id="daf76-142">2</span><span class="sxs-lookup"><span data-stu-id="daf76-142">2</span></span>    |
| <span data-ttu-id="daf76-143">Flap</span><span class="sxs-lookup"><span data-stu-id="daf76-143">Flap</span></span>  | <span data-ttu-id="daf76-144">Colonna8</span><span class="sxs-lookup"><span data-stu-id="daf76-144">Column8</span></span> | <span data-ttu-id="daf76-145">S</span><span class="sxs-lookup"><span data-stu-id="daf76-145">S</span></span>    | <span data-ttu-id="daf76-146">32</span><span class="sxs-lookup"><span data-stu-id="daf76-146">32</span></span>   |



 

<span data-ttu-id="daf76-147">La colonna Version della tabella file può essere una chiave esterna per un altro file nella tabella file.</span><span class="sxs-lookup"><span data-stu-id="daf76-147">The Version column of the File table can be a foreign key to another file in the File table.</span></span> <span data-ttu-id="daf76-148">Questo problema si verifica con i file complementari.</span><span class="sxs-lookup"><span data-stu-id="daf76-148">This occurs with companion files.</span></span> <span data-ttu-id="daf76-149">Tuttavia, la colonna version consente solo una stringa di lunghezza 32, mentre la colonna file consente una stringa di lunghezza 72.</span><span class="sxs-lookup"><span data-stu-id="daf76-149">However, the Version column only allows a string length 32, whereas the File column allows a string length 72.</span></span> <span data-ttu-id="daf76-150">Per correggere questo errore, modificare le lunghezze delle stringhe in modo che corrispondano.</span><span class="sxs-lookup"><span data-stu-id="daf76-150">To fix this error change the string lengths to match.</span></span>

<span data-ttu-id="daf76-151">Sono stati definiti una chiave esterna e una chiave che variano in base ai tipi di definizione.</span><span class="sxs-lookup"><span data-stu-id="daf76-151">There is a foreign key and key defined that differ in their definition types.</span></span> <span data-ttu-id="daf76-152">Column8 della tabella Flap è elencato come chiave esterna per Column1.</span><span class="sxs-lookup"><span data-stu-id="daf76-152">Column8 of the Flap Table is listed as a foreign key to Column1.</span></span> <span data-ttu-id="daf76-153">Column8 è una colonna stringa e Column1 è una colonna di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="daf76-153">Column8 is a string column and Column1 is an integer column.</span></span> <span data-ttu-id="daf76-154">È necessario definire la chiave esterna e le coppie di chiavi in modo che i relativi tipi di dati corrispondano.</span><span class="sxs-lookup"><span data-stu-id="daf76-154">The foreign key and key pairs must be defined so that their data types match.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daf76-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="daf76-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daf76-156">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="daf76-156">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



