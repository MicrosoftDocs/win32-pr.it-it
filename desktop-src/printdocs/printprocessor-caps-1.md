---
description: La \_ struttura PRINTPROCESSOR Caps \_ 1 è il formato per le informazioni sulle funzionalità della stampante restituite dalla funzione GetPrinterData nel buffer specificato dalla variabile pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Struttura PRINTPROCESSOR_CAPS_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316423"
---
# <a name="printprocessor_caps_1-structure"></a><span data-ttu-id="5c874-103">\_Struttura PRINTPROCESSOR Caps \_ 1</span><span class="sxs-lookup"><span data-stu-id="5c874-103">PRINTPROCESSOR\_CAPS\_1 structure</span></span>

<span data-ttu-id="5c874-104">La struttura **PRINTPROCESSOR \_ Caps \_ 1** è il formato per le informazioni sulle funzionalità della stampante restituite dalla funzione [**GetPrinterData**](getprinterdata.md) nel buffer specificato dalla variabile *pData* .</span><span class="sxs-lookup"><span data-stu-id="5c874-104">The **PRINTPROCESSOR\_CAPS\_1** structure is the format for the printer capability information that is returned by the [**GetPrinterData**](getprinterdata.md) function in the buffer specified by the *pData* variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c874-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c874-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a><span data-ttu-id="5c874-106">Members</span><span class="sxs-lookup"><span data-stu-id="5c874-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c874-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="5c874-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="5c874-108">Numero di versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="5c874-108">The structure's version number.</span></span> <span data-ttu-id="5c874-109">Questo valore deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="5c874-109">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="5c874-110">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="5c874-110">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="5c874-111">Maschera di bit che rappresenta i vari numeri di pagine del documento che la stampante è in grado di stampare in una pagina fisica.</span><span class="sxs-lookup"><span data-stu-id="5c874-111">A bit mask representing the various numbers of document pages the printer can print on a physical page.</span></span> <span data-ttu-id="5c874-112">Il bit meno significativo rappresenta 1 pagina documento per pagina, il bit successivo rappresenta 2 pagine documento per pagina e così via.</span><span class="sxs-lookup"><span data-stu-id="5c874-112">The least significant bit represents 1 document page per page, the next bit represents 2 document pages per page, and so on.</span></span> <span data-ttu-id="5c874-113">Ad esempio, 0x0000810B indica che la stampante supporta 1, 2, 4, 9 e 16 pagine documento per ogni pagina fisica.</span><span class="sxs-lookup"><span data-stu-id="5c874-113">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical page.</span></span>

</dd> <dt>

<span data-ttu-id="5c874-114">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="5c874-114">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5c874-115">Ordine in cui verranno stampate le pagine.</span><span class="sxs-lookup"><span data-stu-id="5c874-115">The order in which pages will be printed.</span></span> <span data-ttu-id="5c874-116">Questo valore può essere una stampa normale \_ , una stampa inversa \_ o un opuscolo \_ .</span><span class="sxs-lookup"><span data-stu-id="5c874-116">This value can be NORMAL\_PRINT, REVERSE\_PRINT, or BOOKLET\_PRINT.</span></span>

</dd> <dt>

<span data-ttu-id="5c874-117">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="5c874-117">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="5c874-118">Numero massimo di copie che la stampante è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="5c874-118">The maximum number of copies the printer can handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c874-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c874-119">Remarks</span></span>

<span data-ttu-id="5c874-120">I valori per tutti i membri della struttura sono forniti dalla funzione [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , che è documentata in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="5c874-120">Values for all structure members are supplied by the [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function, which is documented in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="5c874-121">Lo spooler chiama la funzione [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) di un processore di stampa quando un'applicazione chiama [**GetPrinterData**](getprinterdata.md), specificando il nome di un valore con formato PrintProcCaps \_ *DataType*, dove *DataType* è il nome di un tipo di dati di input.</span><span class="sxs-lookup"><span data-stu-id="5c874-121">The spooler calls a print processor's [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function when an application calls [**GetPrinterData**](getprinterdata.md), specifying a value name with a format of PrintProcCaps\_*datatype*, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c874-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c874-122">Requirements</span></span>



| <span data-ttu-id="5c874-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c874-123">Requirement</span></span> | <span data-ttu-id="5c874-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5c874-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c874-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c874-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5c874-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c874-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c874-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c874-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5c874-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c874-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c874-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c874-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c874-130"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c874-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c874-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c874-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c874-132">Stampa</span><span class="sxs-lookup"><span data-stu-id="5c874-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5c874-133">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="5c874-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5c874-134">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="5c874-134">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

