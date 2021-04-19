---
description: Rappresenta le opzioni della stampante.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Struttura PRINTER_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313540"
---
# <a name="printer_options-structure"></a><span data-ttu-id="4a3a5-103">\_Struttura opzioni stampante</span><span class="sxs-lookup"><span data-stu-id="4a3a5-103">PRINTER\_OPTIONS structure</span></span>

<span data-ttu-id="4a3a5-104">Rappresenta le opzioni della stampante.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-104">Represents printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a3a5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a3a5-105">Syntax</span></span>


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="4a3a5-106">Members</span><span class="sxs-lookup"><span data-stu-id="4a3a5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a3a5-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="4a3a5-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a5-108">Dimensione della struttura delle **\_ Opzioni di stampa** .</span><span class="sxs-lookup"><span data-stu-id="4a3a5-108">The size of the **PRINTER\_OPTIONS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a5-109">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="4a3a5-109">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a5-110">Set di [**flag di \_ Opzioni \_ della stampante**](printer-option-flags.md) che specifica il modo in cui l'handle per una stampante restituita da [**OpenPrinter2**](openprinter2.md) verrà usato da altre funzioni.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-110">A set of [**PRINTER\_OPTION\_FLAGS**](printer-option-flags.md) that specifies how the handle to a printer returned by [**OpenPrinter2**](openprinter2.md) will be used by other functions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a3a5-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a3a5-111">Requirements</span></span>



| <span data-ttu-id="4a3a5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a3a5-112">Requirement</span></span> | <span data-ttu-id="4a3a5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4a3a5-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a3a5-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a3a5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4a3a5-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a3a5-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4a3a5-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a3a5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4a3a5-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a3a5-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4a3a5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a3a5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a3a5-119"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a3a5-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a3a5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a3a5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a3a5-121">Stampa</span><span class="sxs-lookup"><span data-stu-id="4a3a5-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4a3a5-122">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4a3a5-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4a3a5-123">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="4a3a5-123">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="4a3a5-124">**\_flag di opzione stampante \_**</span><span class="sxs-lookup"><span data-stu-id="4a3a5-124">**PRINTER\_OPTION\_FLAGS**</span></span>](printer-option-flags.md)
</dt> </dl>

 

 




