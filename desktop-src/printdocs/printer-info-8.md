---
description: La \_ struttura Printer Info \_ 8 specifica le impostazioni della stampante predefinite globali.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Struttura PRINTER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884985"
---
# <a name="printer_info_8-structure"></a><span data-ttu-id="1fe81-103">\_Struttura Info stampante \_ 8</span><span class="sxs-lookup"><span data-stu-id="1fe81-103">PRINTER\_INFO\_8 structure</span></span>

<span data-ttu-id="1fe81-104">La struttura **Printer \_ info \_ 8** specifica le impostazioni della stampante predefinite globali.</span><span class="sxs-lookup"><span data-stu-id="1fe81-104">The **PRINTER\_INFO\_8** structure specifies the global default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe81-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fe81-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="1fe81-106">Members</span><span class="sxs-lookup"><span data-stu-id="1fe81-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1fe81-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="1fe81-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="1fe81-108">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati globali della stampante predefiniti, ad esempio l'orientamento della carta e la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="1fe81-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the global default printer data such as the paper orientation and the resolution.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fe81-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fe81-109">Remarks</span></span>

<span data-ttu-id="1fe81-110">Le impostazioni predefinite globali vengono impostate dall'amministratore di una stampante che può essere usata da chiunque.</span><span class="sxs-lookup"><span data-stu-id="1fe81-110">The global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="1fe81-111">Al contrario, le impostazioni predefinite per singolo utente influiranno su un utente specifico o su qualsiasi altro utente che utilizza il profilo.</span><span class="sxs-lookup"><span data-stu-id="1fe81-111">In contrast, the per-user defaults will affect a particular user or anyone else who uses the profile.</span></span> <span data-ttu-id="1fe81-112">Per le impostazioni predefinite per utente, usare [**le \_ informazioni \_ sulla stampante 9**](printer-info-9.md).</span><span class="sxs-lookup"><span data-stu-id="1fe81-112">For per-user defaults, use [**PRINTER\_INFO\_9**](printer-info-9.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe81-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fe81-113">Requirements</span></span>



| <span data-ttu-id="1fe81-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fe81-114">Requirement</span></span> | <span data-ttu-id="1fe81-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1fe81-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe81-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fe81-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe81-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1fe81-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1fe81-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fe81-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe81-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1fe81-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1fe81-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fe81-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fe81-121"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fe81-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1fe81-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1fe81-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1fe81-123">**\_ Informazioni sulle stampanti \_ \_ 8W** (Unicode) e **\_ informazioni sulla stampante \_ \_ 8a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1fe81-123">**\_PRINTER\_INFO\_8W** (Unicode) and **\_PRINTER\_INFO\_8A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="1fe81-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fe81-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe81-125">Stampa</span><span class="sxs-lookup"><span data-stu-id="1fe81-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1fe81-126">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="1fe81-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1fe81-127">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="1fe81-127">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="1fe81-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="1fe81-128">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="1fe81-129">**Informazioni sulla stampante \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="1fe81-129">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> </dl>

 

 




