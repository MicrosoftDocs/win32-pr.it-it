---
description: Specifica la memorizzazione nella cache di un handle per una stampante aperta con OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Enumerazione PRINTER_OPTION_FLAGS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233042"
---
# <a name="printer_option_flags-enumeration"></a><span data-ttu-id="a62ed-103">\_ \_ Enumerazione flag opzioni stampante</span><span class="sxs-lookup"><span data-stu-id="a62ed-103">PRINTER\_OPTION\_FLAGS enumeration</span></span>

<span data-ttu-id="a62ed-104">Specifica la memorizzazione nella cache di un handle per una stampante aperta con [**OpenPrinter2**](openprinter2.md).</span><span class="sxs-lookup"><span data-stu-id="a62ed-104">Specifies the caching of a handle for a printer opened with [**OpenPrinter2**](openprinter2.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a62ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a62ed-105">Syntax</span></span>


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="a62ed-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="a62ed-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a62ed-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**\_opzione stampante \_ senza \_ cache**</span><span class="sxs-lookup"><span data-stu-id="a62ed-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**PRINTER\_OPTION\_NO\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="a62ed-108">L'handle non viene memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="a62ed-108">The handle is not cached.</span></span> <span data-ttu-id="a62ed-109">Tutte le funzioni applicate a un handle restituito da [**OpenPrinter2**](openprinter2.md) verranno inviate al computer remoto.</span><span class="sxs-lookup"><span data-stu-id="a62ed-109">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="a62ed-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_cache delle opzioni della stampante \_**</span><span class="sxs-lookup"><span data-stu-id="a62ed-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**PRINTER\_OPTION\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="a62ed-111">L'handle viene memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="a62ed-111">The handle is cached.</span></span> <span data-ttu-id="a62ed-112">Tutte le funzioni applicate a un handle restituito da [**OpenPrinter2**](openprinter2.md) verranno inviate alla cache locale.</span><span class="sxs-lookup"><span data-stu-id="a62ed-112">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the local cache.</span></span>

</dd> <dt>

<span data-ttu-id="a62ed-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**\_opzione stampante \_ - \_ modifica client**</span><span class="sxs-lookup"><span data-stu-id="a62ed-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**PRINTER\_OPTION\_CLIENT\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="a62ed-114">L'handle restituito da [**OpenPrinter2**](openprinter2.md) può essere usato da [**seprinter**](setprinter.md) per rinominare la connessione alla stampante.</span><span class="sxs-lookup"><span data-stu-id="a62ed-114">The handle returned by [**OpenPrinter2**](openprinter2.md) can be used by [**SetPrinter**](setprinter.md) to rename the printer connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a62ed-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a62ed-115">Requirements</span></span>



| <span data-ttu-id="a62ed-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a62ed-116">Requirement</span></span> | <span data-ttu-id="a62ed-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a62ed-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a62ed-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a62ed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a62ed-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a62ed-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a62ed-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a62ed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a62ed-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a62ed-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a62ed-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a62ed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a62ed-123"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a62ed-123"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a62ed-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a62ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62ed-125">Stampa</span><span class="sxs-lookup"><span data-stu-id="a62ed-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a62ed-126">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="a62ed-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a62ed-127">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="a62ed-127">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="a62ed-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="a62ed-128">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




