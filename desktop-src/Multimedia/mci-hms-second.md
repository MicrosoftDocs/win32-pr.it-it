---
title: MCI_HMS_SECOND macro (Mciapi. h)
description: La \_ macro MCI HMS \_ Second Recupera il componente secondi da un parametro contenente le informazioni relative a ore/minuti/secondi (HMS) compressi.
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874558"
---
# <a name="mci_hms_second-macro"></a><span data-ttu-id="54143-104">\_Terza macro MCI HMS \_ Second</span><span class="sxs-lookup"><span data-stu-id="54143-104">MCI\_HMS\_SECOND macro</span></span>

<span data-ttu-id="54143-105">La macro **MCI \_ HMS \_ Second** Recupera il componente secondi da un parametro contenente le informazioni relative a ore/minuti/secondi (HMS) compressi.</span><span class="sxs-lookup"><span data-stu-id="54143-105">The **MCI\_HMS\_SECOND** macro retrieves the seconds component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="54143-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54143-106">Syntax</span></span>


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="54143-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="54143-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54143-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="54143-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="54143-109">Tempo in formato HMS.</span><span class="sxs-lookup"><span data-stu-id="54143-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54143-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54143-110">Return value</span></span>

<span data-ttu-id="54143-111">Restituisce il componente relativo ai secondi delle informazioni di HMS specificate.</span><span class="sxs-lookup"><span data-stu-id="54143-111">Returns the seconds component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="54143-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="54143-112">Remarks</span></span>

<span data-ttu-id="54143-113">L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente le ore, il successivo byte meno significativo che contiene minuti e il successivo byte meno significativo contenente i secondi.</span><span class="sxs-lookup"><span data-stu-id="54143-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="54143-114">Il byte più significativo è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="54143-114">The most significant byte is unused.</span></span>

<span data-ttu-id="54143-115">La macro **MCI \_ HMS \_ Second** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="54143-115">The **MCI\_HMS\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="54143-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54143-116">Requirements</span></span>



| <span data-ttu-id="54143-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="54143-117">Requirement</span></span> | <span data-ttu-id="54143-118">Valore</span><span class="sxs-lookup"><span data-stu-id="54143-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="54143-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54143-119">Minimum supported client</span></span><br/> | <span data-ttu-id="54143-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54143-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="54143-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54143-121">Minimum supported server</span></span><br/> | <span data-ttu-id="54143-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54143-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="54143-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54143-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="54143-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="54143-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54143-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54143-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54143-126">MCI</span><span class="sxs-lookup"><span data-stu-id="54143-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="54143-127">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="54143-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





