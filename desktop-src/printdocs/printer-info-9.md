---
description: La \_ struttura Printer Info \_ 9 specifica le impostazioni predefinite della stampante per singolo utente.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Struttura PRINTER_INFO_9 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318028"
---
# <a name="printer_info_9-structure"></a><span data-ttu-id="068ae-103">Struttura delle informazioni di stampa \_ \_ 9</span><span class="sxs-lookup"><span data-stu-id="068ae-103">PRINTER\_INFO\_9 structure</span></span>

<span data-ttu-id="068ae-104">La struttura **Printer \_ info \_ 9** specifica le impostazioni predefinite della stampante per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="068ae-104">The **PRINTER\_INFO\_9** structure specifies the per-user default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="068ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="068ae-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a><span data-ttu-id="068ae-106">Members</span><span class="sxs-lookup"><span data-stu-id="068ae-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="068ae-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="068ae-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="068ae-108">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati della stampante predefiniti per ogni utente, ad esempio l'orientamento della carta e la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="068ae-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the per-user default printer data such as the paper orientation and the resolution.</span></span> <span data-ttu-id="068ae-109">**DEVMODE** viene archiviato nel registro di sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="068ae-109">The **DEVMODE** is stored in the user's registry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="068ae-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="068ae-110">Remarks</span></span>

<span data-ttu-id="068ae-111">Le impostazioni predefinite per utente avranno effetto solo su un utente specifico o su chiunque utilizzi il profilo.</span><span class="sxs-lookup"><span data-stu-id="068ae-111">The per-user defaults will affect only a particular user or anyone who uses the profile.</span></span> <span data-ttu-id="068ae-112">Al contrario, le impostazioni predefinite globali vengono impostate dall'amministratore di una stampante che può essere utilizzata da chiunque.</span><span class="sxs-lookup"><span data-stu-id="068ae-112">In contrast, the global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="068ae-113">Per le impostazioni predefinite globali, usare le [**informazioni sulla stampante \_ \_ 8**](printer-info-8.md).</span><span class="sxs-lookup"><span data-stu-id="068ae-113">For global defaults, use [**PRINTER\_INFO\_8**](printer-info-8.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="068ae-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="068ae-114">Requirements</span></span>



| <span data-ttu-id="068ae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="068ae-115">Requirement</span></span> | <span data-ttu-id="068ae-116">Valore</span><span class="sxs-lookup"><span data-stu-id="068ae-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="068ae-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="068ae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="068ae-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="068ae-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="068ae-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="068ae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="068ae-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="068ae-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="068ae-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="068ae-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="068ae-122"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="068ae-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="068ae-123">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="068ae-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="068ae-124">**\_ Informazioni sulle stampanti \_ \_ 9W** (Unicode) e **\_ informazioni sulla stampante \_ \_ 9a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="068ae-124">**\_PRINTER\_INFO\_9W** (Unicode) and **\_PRINTER\_INFO\_9A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="068ae-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="068ae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068ae-126">Stampa</span><span class="sxs-lookup"><span data-stu-id="068ae-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="068ae-127">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="068ae-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="068ae-128">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="068ae-128">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="068ae-129">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="068ae-129">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="068ae-130">**\_Informazioni stampante \_ 8**</span><span class="sxs-lookup"><span data-stu-id="068ae-130">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> </dl>

 

 




