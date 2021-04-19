---
description: Rappresenta un driver della stampante da cui dipendono altri driver della stampante.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Struttura CORE_PRINTER_DRIVER (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311829"
---
# <a name="core_printer_driver-structure"></a><span data-ttu-id="9d5c3-103">\_Struttura driver della stampante principale \_</span><span class="sxs-lookup"><span data-stu-id="9d5c3-103">CORE\_PRINTER\_DRIVER structure</span></span>

<span data-ttu-id="9d5c3-104">Rappresenta un driver della stampante da cui dipendono altri driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-104">Represents a printer driver on which other printer drivers depend.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d5c3-105">Syntax</span></span>


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a><span data-ttu-id="9d5c3-106">Members</span><span class="sxs-lookup"><span data-stu-id="9d5c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d5c3-107">**CoreDriverGUID**</span><span class="sxs-lookup"><span data-stu-id="9d5c3-107">**CoreDriverGUID**</span></span>
</dt> <dd>

<span data-ttu-id="9d5c3-108">GUID del driver della stampante principale.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-108">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="9d5c3-109">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="9d5c3-109">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="9d5c3-110">Data e ora dell'ultima versione del driver della stampante principale.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-110">The date and time of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="9d5c3-111">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="9d5c3-111">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9d5c3-112">ID versione della versione più recente del driver della stampante principale.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-112">The version ID of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="9d5c3-113">**\[percorso massimo \_ szPackageID\]**</span><span class="sxs-lookup"><span data-stu-id="9d5c3-113">**szPackageID\[MAX\_PATH\]**</span></span>
</dt> <dd>

<span data-ttu-id="9d5c3-114">Percorso del pacchetto driver che contiene il driver della stampante principale.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-114">The path to the driver package that contains the core printer driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d5c3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d5c3-115">Remarks</span></span>

<span data-ttu-id="9d5c3-116">Questa struttura può rappresentare un driver di base del produttore su cui dipendono i driver per diversi modelli di stampante.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-116">This structure can represent a manufacturer's base driver on which the drivers for various printer models are dependent.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5c3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d5c3-117">Requirements</span></span>



| <span data-ttu-id="9d5c3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d5c3-118">Requirement</span></span> | <span data-ttu-id="9d5c3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9d5c3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5c3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d5c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5c3-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d5c3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9d5c3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d5c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5c3-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d5c3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d5c3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d5c3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5c3-125"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d5c3-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9d5c3-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9d5c3-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d5c3-127">**\_ Core \_ Printer \_ DRIVERW** (Unicode) e **\_ Core \_ Printer \_ drivera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9d5c3-127">**\_CORE\_PRINTER\_DRIVERW** (Unicode) and **\_CORE\_PRINTER\_DRIVERA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9d5c3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d5c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5c3-129">Stampa</span><span class="sxs-lookup"><span data-stu-id="9d5c3-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9d5c3-130">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="9d5c3-130">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




