---
description: La struttura Datatypes \_ info \_ 1 contiene informazioni sul tipo di dati utilizzato per registrare un processo di stampa.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: Struttura DATATYPES_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227475"
---
# <a name="datatypes_info_1-structure"></a><span data-ttu-id="b3524-103">Struttura di informazioni sui tipi di \_ dati \_ 1</span><span class="sxs-lookup"><span data-stu-id="b3524-103">DATATYPES\_INFO\_1 structure</span></span>

<span data-ttu-id="b3524-104">La struttura **DATAtypes \_ info \_ 1** contiene informazioni sul tipo di dati utilizzato per registrare un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="b3524-104">The **DATATYPES\_INFO\_1** structure contains information about the data type used to record a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3524-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3524-105">Syntax</span></span>


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a><span data-ttu-id="b3524-106">Members</span><span class="sxs-lookup"><span data-stu-id="b3524-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3524-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="b3524-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="b3524-108">Puntatore a una stringa con terminazione null che identifica il tipo di dati utilizzato per registrare un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="b3524-108">Pointer to a null-terminated string that identifies the data type used to record a print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3524-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3524-109">Requirements</span></span>



| <span data-ttu-id="b3524-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3524-110">Requirement</span></span> | <span data-ttu-id="b3524-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b3524-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3524-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3524-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b3524-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b3524-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b3524-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3524-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b3524-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b3524-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b3524-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3524-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3524-117"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3524-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b3524-118">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b3524-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b3524-119">**\_ Tipi di \_ dati info \_ 1W** (Unicode) e **\_ DataTypes \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b3524-119">**\_DATATYPES\_INFO\_1W** (Unicode) and **\_DATATYPES\_INFO\_1A** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b3524-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3524-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3524-121">Stampa</span><span class="sxs-lookup"><span data-stu-id="b3524-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b3524-122">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="b3524-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b3524-123">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="b3524-123">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




