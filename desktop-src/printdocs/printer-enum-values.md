---
description: La \_ struttura Printer enum \_ values specifica il nome del valore, il tipo e i dati per un valore di configurazione della stampante restituito dalla funzione EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Struttura PRINTER_ENUM_VALUES (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314004"
---
# <a name="printer_enum_values-structure"></a><span data-ttu-id="fa92b-103">\_ \_ Struttura dei valori enum della stampante</span><span class="sxs-lookup"><span data-stu-id="fa92b-103">PRINTER\_ENUM\_VALUES structure</span></span>

<span data-ttu-id="fa92b-104">La struttura **Printer \_ enum \_ values** specifica il nome del valore, il tipo e i dati per un valore di configurazione della stampante restituito dalla funzione [**EnumPrinterDataEx**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="fa92b-104">The **PRINTER\_ENUM\_VALUES** structure specifies the value name, type, and data for a printer configuration value returned by the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa92b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa92b-105">Syntax</span></span>


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a><span data-ttu-id="fa92b-106">Members</span><span class="sxs-lookup"><span data-stu-id="fa92b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa92b-107">**pValueName**</span><span class="sxs-lookup"><span data-stu-id="fa92b-107">**pValueName**</span></span>
</dt> <dd>

<span data-ttu-id="fa92b-108">Puntatore a una stringa con terminazione null che specifica il nome del valore recuperato.</span><span class="sxs-lookup"><span data-stu-id="fa92b-108">Pointer to a null-terminated string that specifies the name of the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="fa92b-109">**cbValueName**</span><span class="sxs-lookup"><span data-stu-id="fa92b-109">**cbValueName**</span></span>
</dt> <dd>

<span data-ttu-id="fa92b-110">Numero di byte nel membro **pValueName** , incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="fa92b-110">The number of bytes in the **pValueName** member, including the terminating NULL character.</span></span>

</dd> <dt>

<span data-ttu-id="fa92b-111">**dwType**</span><span class="sxs-lookup"><span data-stu-id="fa92b-111">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="fa92b-112">Codice che indica il tipo di dati a cui fa riferimento il membro **pData** .</span><span class="sxs-lookup"><span data-stu-id="fa92b-112">A code indicating the type of data pointed to by the **pData** member.</span></span> <span data-ttu-id="fa92b-113">Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="fa92b-113">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="fa92b-114">**pData**</span><span class="sxs-lookup"><span data-stu-id="fa92b-114">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="fa92b-115">Puntatore a un buffer contenente i dati per il valore recuperato.</span><span class="sxs-lookup"><span data-stu-id="fa92b-115">Pointer to a buffer containing the data for the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="fa92b-116">**cbData**</span><span class="sxs-lookup"><span data-stu-id="fa92b-116">**cbData**</span></span>
</dt> <dd>

<span data-ttu-id="fa92b-117">Numero di byte recuperati nel buffer **pData** .</span><span class="sxs-lookup"><span data-stu-id="fa92b-117">The number of bytes retrieved in the **pData** buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa92b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa92b-118">Requirements</span></span>



| <span data-ttu-id="fa92b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa92b-119">Requirement</span></span> | <span data-ttu-id="fa92b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fa92b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa92b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa92b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fa92b-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa92b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa92b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa92b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fa92b-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa92b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa92b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa92b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa92b-126"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa92b-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fa92b-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="fa92b-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fa92b-128">**\_ Printer \_ enum \_ VALUESW** (Unicode) e **\_ Printer \_ enum \_ values** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fa92b-128">**\_PRINTER\_ENUM\_VALUESW** (Unicode) and **\_PRINTER\_ENUM\_VALUESA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fa92b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa92b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa92b-130">Stampa</span><span class="sxs-lookup"><span data-stu-id="fa92b-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fa92b-131">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="fa92b-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="fa92b-132">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="fa92b-132">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> </dl>

 

