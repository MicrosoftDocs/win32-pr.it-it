---
description: Rappresenta le informazioni sulla funzionalità della stampante.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Struttura PRINTPROCESSOR_CAPS_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315981"
---
# <a name="printprocessor_caps_2-structure"></a><span data-ttu-id="81a52-103">\_Struttura PRINTPROCESSOR Caps \_ 2</span><span class="sxs-lookup"><span data-stu-id="81a52-103">PRINTPROCESSOR\_CAPS\_2 structure</span></span>

<span data-ttu-id="81a52-104">Rappresenta le informazioni sulla funzionalità della stampante.</span><span class="sxs-lookup"><span data-stu-id="81a52-104">Represents printer capability information.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81a52-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a><span data-ttu-id="81a52-106">Members</span><span class="sxs-lookup"><span data-stu-id="81a52-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="81a52-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="81a52-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="81a52-108">Valore che indica il numero di versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="81a52-108">A value that indicates the structure's version number.</span></span>

</dd> <dt>

<span data-ttu-id="81a52-109">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="81a52-109">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="81a52-110">Maschera di bit che rappresenta i vari numeri di pagine del documento che la stampante è in grado di stampare su un solo lato di un foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="81a52-110">A bit mask representing the various numbers of document pages the printer can print on a single side of a physical sheet.</span></span> <span data-ttu-id="81a52-111">Il bit meno significativo rappresenta una pagina del documento per lato, il bit successivo rappresenta 2 pagine del documento per lato e così via.</span><span class="sxs-lookup"><span data-stu-id="81a52-111">The least significant bit represents one document page per side, the next bit represents 2 document pages per side, and so on.</span></span> <span data-ttu-id="81a52-112">Ad esempio, 0x0000810B indica che la stampante supporta 1, 2, 4, 9 e 16 pagine documento per lato fisico.</span><span class="sxs-lookup"><span data-stu-id="81a52-112">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical side.</span></span>

</dd> <dt>

<span data-ttu-id="81a52-113">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="81a52-113">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="81a52-114">Valore del flag che indica l'ordine in cui verranno stampate le pagine.</span><span class="sxs-lookup"><span data-stu-id="81a52-114">A flag value that indicates the order in which pages will be printed.</span></span> <span data-ttu-id="81a52-115">Può essere stampa **normale \_**, **\_ Stampa inversa** o **opuscolo \_**.</span><span class="sxs-lookup"><span data-stu-id="81a52-115">It can be **NORMAL\_PRINT**, **REVERSE\_PRINT**, or **BOOKLET\_PRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="81a52-116">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="81a52-116">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="81a52-117">Numero massimo di copie che la stampante è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="81a52-117">The maximum number of copies the printer can handle.</span></span>

</dd> <dt>

<span data-ttu-id="81a52-118">**dwNupDirectionCaps**</span><span class="sxs-lookup"><span data-stu-id="81a52-118">**dwNupDirectionCaps**</span></span>
</dt> <dd>

<span data-ttu-id="81a52-119">Modelli disponibili quando più pagine del documento vengono stampate sullo stesso lato di un foglio di carta.</span><span class="sxs-lookup"><span data-stu-id="81a52-119">The available patterns when multiple document pages are printed on the same side of a sheet of paper.</span></span> <span data-ttu-id="81a52-120">I flag possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="81a52-120">The possible flags are the following:</span></span>



| <span data-ttu-id="81a52-121">Valore</span><span class="sxs-lookup"><span data-stu-id="81a52-121">Value</span></span>                     | <span data-ttu-id="81a52-122">Significato</span><span class="sxs-lookup"><span data-stu-id="81a52-122">Meaning</span></span>                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a52-123">PPCAPS \_ subito \_ dopo \_</span><span class="sxs-lookup"><span data-stu-id="81a52-123">PPCAPS\_RIGHT\_THEN\_DOWN</span></span> | <span data-ttu-id="81a52-124">Le pagine vengono visualizzate in righe da destra a sinistra, ogni riga successiva al di sotto del suo predecessore.</span><span class="sxs-lookup"><span data-stu-id="81a52-124">Pages appear in rows from right to left, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="81a52-125">PPCAPS \_ giù \_ a \_ destra</span><span class="sxs-lookup"><span data-stu-id="81a52-125">PPCAPS\_DOWN\_THEN\_RIGHT</span></span> | <span data-ttu-id="81a52-126">Le pagine vengono visualizzate in colonne dall'alto verso il basso, ciascuna colonna successiva a destra del relativo predecessore.</span><span class="sxs-lookup"><span data-stu-id="81a52-126">Pages appear in columns from top to bottom, each subsequent column to the right of its predecessor.</span></span> |
| <span data-ttu-id="81a52-127">PPCAPS verso il \_ \_ \_ basso</span><span class="sxs-lookup"><span data-stu-id="81a52-127">PPCAPS\_LEFT\_THEN\_DOWN</span></span>  | <span data-ttu-id="81a52-128">Le pagine vengono visualizzate in righe da sinistra a destra, ogni riga successiva al di sotto del suo predecessore.</span><span class="sxs-lookup"><span data-stu-id="81a52-128">Pages appear in rows from left to right, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="81a52-129">PPCAPS \_ a \_ \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="81a52-129">PPCAPS\_DOWN\_THEN\_LEFT</span></span>  | <span data-ttu-id="81a52-130">Le pagine vengono visualizzate in colonne dall'alto verso il basso, ogni colonna successiva a sinistra del relativo predecessore.</span><span class="sxs-lookup"><span data-stu-id="81a52-130">Pages appear in columns from top to bottom, each subsequent column to the left of its predecessor.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="81a52-131">**dwNupBorderCaps**</span><span class="sxs-lookup"><span data-stu-id="81a52-131">**dwNupBorderCaps**</span></span>
</dt> <dd>

<span data-ttu-id="81a52-132">Può essere solo \_ Stampa bordo PPCAPS \_ , a indicare che, quando vengono stampate più pagine del documento su un solo lato di un foglio fisico, è possibile indicare alla stampante se stampare un bordo intorno all'area stampabile di ogni pagina del documento.</span><span class="sxs-lookup"><span data-stu-id="81a52-132">Can be only PPCAPS\_BORDER\_PRINT, indicating that, when multiple document pages are being printed on a single side of a physical sheet, the printer can be told whether or not to print a border around the imageable area of each document page.</span></span>

</dd> <dt>

<span data-ttu-id="81a52-133">**dwBookletHandlingCaps**</span><span class="sxs-lookup"><span data-stu-id="81a52-133">**dwBookletHandlingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="81a52-134">Può essere PPCAPS solo \_ per \_ il bordo dell'opuscolo, a indicare che la stampante può stampare lo stile del libretto.</span><span class="sxs-lookup"><span data-stu-id="81a52-134">Can only be PPCAPS\_BOOKLET\_EDGE, indicating that the printer can print booklet style.</span></span>

<span data-ttu-id="81a52-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span><span class="sxs-lookup"><span data-stu-id="81a52-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span></span><dd> 

| <span data-ttu-id="81a52-136">Valore</span><span class="sxs-lookup"><span data-stu-id="81a52-136">Value</span></span>                                         | <span data-ttu-id="81a52-137">Significato</span><span class="sxs-lookup"><span data-stu-id="81a52-137">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a52-138">PPCAPS \_ le \_ pagine inverse \_ per \_ duplex invertito \_</span><span class="sxs-lookup"><span data-stu-id="81a52-138">PPCAPS\_REVERSE\_PAGES\_FOR\_REVERSE\_DUPLEX</span></span>  | <span data-ttu-id="81a52-139">Quando si esegue la stampa in ordine inverso e duplexing, il processore può stampare lo swap dell'ordine di ogni coppia di pagine, quindi anziché stampare nell'ordine 4, 3, 2, 1, verranno stampate nell'ordine 3, 4, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="81a52-139">When printing in reverse order and duplexing, the processor can print swap the order of each pair of pages, so instead of printing in order 4,3,2,1, they will print in the order 3,4,1,2.</span></span>                                                                                                       |
| <span data-ttu-id="81a52-140">PPCAPS \_ non \_ inviano \_ \_ pagine aggiuntive \_ per \_ duplex</span><span class="sxs-lookup"><span data-stu-id="81a52-140">PPCAPS\_DONT\_SEND\_EXTRA\_PAGES\_FOR\_DUPLEX</span></span> | <span data-ttu-id="81a52-141">Quando si esegue la duplexing, il processore di stampa può essere avvisato di non inviare una pagina aggiuntiva quando è presente un numero dispari di pagine documento.</span><span class="sxs-lookup"><span data-stu-id="81a52-141">When duplexing, the Print Processor can be told not to send an extra page when there is an odd number of document pages.</span></span> <span data-ttu-id="81a52-142">Il processore rispetterà il valore nel modo migliore possibile, ma nei casi in cui impedire una pagina vuota aggiuntiva potrebbe causare un output non corretto, le pagine aggiuntive potrebbero essere ancora inviate.</span><span class="sxs-lookup"><span data-stu-id="81a52-142">The processor will honor the value as best as it can, but in cases where preventing an extra blank page would cause improper output, the extra pages may still be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="81a52-143">**dwScalingCaps**</span><span class="sxs-lookup"><span data-stu-id="81a52-143">**dwScalingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="81a52-144">Può essere PPCAPS solo \_ il \_ ridimensionamento quadrato, a indicare che la stampante può ridimensionare l'immagine della pagina.</span><span class="sxs-lookup"><span data-stu-id="81a52-144">Can only be PPCAPS\_SQUARE\_SCALING, indicating that the printer can scale the page image.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81a52-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="81a52-145">Remarks</span></span>

<span data-ttu-id="81a52-146">I valori per tutti i membri della struttura sono forniti dalla funzione **GetPrintProcessorCapabilities** , documentata in Windows Driver Kit.</span><span class="sxs-lookup"><span data-stu-id="81a52-146">Values for all structure members are supplied by the **GetPrintProcessorCapabilities** function which is documented in the Windows Driver Kit.</span></span>

<span data-ttu-id="81a52-147">Quando un'applicazione chiama [**GetPrinterData**](getprinterdata.md), lo spooler chiama la funzione **GetPrintProcessorCapabilities** di un processore di stampa e specifica un nome di valore con formato **PrintProcCaps \_**_DataType_, dove *DataType* è il nome di un tipo di dati di input.</span><span class="sxs-lookup"><span data-stu-id="81a52-147">When an application calls [**GetPrinterData**](getprinterdata.md), the spooler calls a print processor's **GetPrintProcessorCapabilities** function and specifies a value name that has a format of **PrintProcCaps\_**_datatype_, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a52-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81a52-148">Requirements</span></span>



| <span data-ttu-id="81a52-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a52-149">Requirement</span></span> | <span data-ttu-id="81a52-150">Valore</span><span class="sxs-lookup"><span data-stu-id="81a52-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a52-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81a52-151">Minimum supported client</span></span><br/> | <span data-ttu-id="81a52-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81a52-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="81a52-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81a52-153">Minimum supported server</span></span><br/> | <span data-ttu-id="81a52-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81a52-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="81a52-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81a52-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="81a52-156"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81a52-156"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a52-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81a52-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a52-158">Stampa</span><span class="sxs-lookup"><span data-stu-id="81a52-158">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="81a52-159">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="81a52-159">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="81a52-160">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="81a52-160">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

 




