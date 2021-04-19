---
description: La \_ struttura Port info \_ 1 identifica una porta stampante supportata.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: Struttura PORT_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311814"
---
# <a name="port_info_1-structure"></a><span data-ttu-id="ecedc-103">Struttura delle informazioni sulla porta \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="ecedc-103">PORT\_INFO\_1 structure</span></span>

<span data-ttu-id="ecedc-104">La struttura **Port \_ info \_ 1** identifica una porta stampante supportata.</span><span class="sxs-lookup"><span data-stu-id="ecedc-104">The **PORT\_INFO\_1** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecedc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecedc-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a><span data-ttu-id="ecedc-106">Members</span><span class="sxs-lookup"><span data-stu-id="ecedc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ecedc-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="ecedc-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ecedc-108">Puntatore a una stringa con terminazione null che identifica una porta stampante supportata (ad esempio, "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="ecedc-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecedc-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecedc-109">Requirements</span></span>



| <span data-ttu-id="ecedc-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecedc-110">Requirement</span></span> | <span data-ttu-id="ecedc-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ecedc-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecedc-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecedc-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ecedc-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ecedc-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ecedc-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecedc-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ecedc-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ecedc-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ecedc-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecedc-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecedc-117"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecedc-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ecedc-118">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ecedc-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ecedc-119">**\_ \_ Info porta \_ 1W** (Unicode) e **\_ porta \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ecedc-119">**\_PORT\_INFO\_1W** (Unicode) and **\_PORT\_INFO\_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="ecedc-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecedc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecedc-121">Stampa</span><span class="sxs-lookup"><span data-stu-id="ecedc-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ecedc-122">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="ecedc-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ecedc-123">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="ecedc-123">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




