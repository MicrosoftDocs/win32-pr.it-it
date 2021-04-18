---
description: La \_ struttura informazioni driver \_ 1 identifica un driver della stampante.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: Struttura DRIVER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317297"
---
# <a name="driver_info_1-structure"></a><span data-ttu-id="56d03-103">\_Struttura informazioni driver \_ 1</span><span class="sxs-lookup"><span data-stu-id="56d03-103">DRIVER\_INFO\_1 structure</span></span>

<span data-ttu-id="56d03-104">La **struttura \_ informazioni driver \_ 1** identifica un driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="56d03-104">The **DRIVER\_INFO\_1** structure identifies a printer driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d03-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56d03-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="56d03-106">Members</span><span class="sxs-lookup"><span data-stu-id="56d03-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="56d03-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="56d03-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="56d03-108">Puntatore a una stringa con terminazione null che specifica il nome di un driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="56d03-108">Pointer to a null-terminated string that specifies the name of a printer driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56d03-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56d03-109">Requirements</span></span>



| <span data-ttu-id="56d03-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="56d03-110">Requirement</span></span> | <span data-ttu-id="56d03-111">Valore</span><span class="sxs-lookup"><span data-stu-id="56d03-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56d03-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56d03-112">Minimum supported client</span></span><br/> | <span data-ttu-id="56d03-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="56d03-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56d03-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56d03-114">Minimum supported server</span></span><br/> | <span data-ttu-id="56d03-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="56d03-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="56d03-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56d03-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="56d03-117"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56d03-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="56d03-118">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="56d03-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="56d03-119">**\_ Informazioni sul driver \_ \_ 1W** (Unicode) e **\_ informazioni sul driver \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="56d03-119">**\_DRIVER\_INFO\_1W** (Unicode) and **\_DRIVER\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="56d03-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56d03-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d03-121">Stampa</span><span class="sxs-lookup"><span data-stu-id="56d03-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="56d03-122">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="56d03-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="56d03-123">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="56d03-123">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

 




