---
description: Indica lo stato corrente di un esperto in esecuzione.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Struttura EXPERTSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525158"
---
# <a name="expertstatus-structure"></a><span data-ttu-id="e4462-103">Struttura EXPERTSTATUS</span><span class="sxs-lookup"><span data-stu-id="e4462-103">EXPERTSTATUS structure</span></span>

<span data-ttu-id="e4462-104">La struttura **EXPERTSTATUS** indica lo stato corrente di un esperto in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e4462-104">The **EXPERTSTATUS** structure indicates the current status of a running expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4462-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4462-105">Syntax</span></span>


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a><span data-ttu-id="e4462-106">Members</span><span class="sxs-lookup"><span data-stu-id="e4462-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e4462-107">**Status**</span><span class="sxs-lookup"><span data-stu-id="e4462-107">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="e4462-108">Valore di stato esperto corrente definito dall'enumerazione [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="e4462-108">Current expert status value defined by the [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e4462-109">**Stato secondario**</span><span class="sxs-lookup"><span data-stu-id="e4462-109">**SubStatus**</span></span>
</dt> <dd>

<span data-ttu-id="e4462-110">Valore di stato secondario.</span><span class="sxs-lookup"><span data-stu-id="e4462-110">Sub-status value.</span></span>

</dd> <dt>

<span data-ttu-id="e4462-111">**PercentDone**</span><span class="sxs-lookup"><span data-stu-id="e4462-111">**PercentDone**</span></span>
</dt> <dd>

<span data-ttu-id="e4462-112">Percentuale di completamento dell'analisi di esperti dei dati di rete.</span><span class="sxs-lookup"><span data-stu-id="e4462-112">Percentage completion of the expert analysis of network data.</span></span>

</dd> <dt>

<span data-ttu-id="e4462-113">**Frame**</span><span class="sxs-lookup"><span data-stu-id="e4462-113">**Frame**</span></span>
</dt> <dd>

<span data-ttu-id="e4462-114">Numero di frame.</span><span class="sxs-lookup"><span data-stu-id="e4462-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="e4462-115">**szStatusText**</span><span class="sxs-lookup"><span data-stu-id="e4462-115">**szStatusText**</span></span>
</dt> <dd>

<span data-ttu-id="e4462-116">Testo che descrive lo stato dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="e4462-116">Text that describes the expert status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4462-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4462-117">Requirements</span></span>



| <span data-ttu-id="e4462-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4462-118">Requirement</span></span> | <span data-ttu-id="e4462-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e4462-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e4462-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4462-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4462-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e4462-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e4462-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4462-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4462-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e4462-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e4462-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4462-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4462-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4462-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




