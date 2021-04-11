---
title: MCI_HMS_MINUTE macro (Mciapi. h)
description: La \_ macro MCI HMS \_ minute Recupera il componente minuti da un parametro che contiene le informazioni relative a ore/minuti/secondi (HMS) compressi.
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121458"
---
# <a name="mci_hms_minute-macro"></a><span data-ttu-id="8835b-104">Macro di MCI \_ HMS \_ minute</span><span class="sxs-lookup"><span data-stu-id="8835b-104">MCI\_HMS\_MINUTE macro</span></span>

<span data-ttu-id="8835b-105">La macro **MCI \_ HMS \_ minute** Recupera il componente minuti da un parametro che contiene le informazioni relative a ore/minuti/secondi (HMS) compressi.</span><span class="sxs-lookup"><span data-stu-id="8835b-105">The **MCI\_HMS\_MINUTE** macro retrieves the minutes component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8835b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8835b-106">Syntax</span></span>


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="8835b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8835b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8835b-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="8835b-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="8835b-109">Tempo in formato HMS.</span><span class="sxs-lookup"><span data-stu-id="8835b-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8835b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8835b-110">Return value</span></span>

<span data-ttu-id="8835b-111">Restituisce il componente minuti delle informazioni di HMS specificate.</span><span class="sxs-lookup"><span data-stu-id="8835b-111">Returns the minutes component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="8835b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8835b-112">Remarks</span></span>

<span data-ttu-id="8835b-113">L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente le ore, il successivo byte meno significativo che contiene minuti e il successivo byte meno significativo contenente i secondi.</span><span class="sxs-lookup"><span data-stu-id="8835b-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="8835b-114">Il byte più significativo è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="8835b-114">The most significant byte is unused.</span></span>

<span data-ttu-id="8835b-115">La macro **MCI \_ HMS \_ minute** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8835b-115">The **MCI\_HMS\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="8835b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8835b-116">Requirements</span></span>



| <span data-ttu-id="8835b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8835b-117">Requirement</span></span> | <span data-ttu-id="8835b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8835b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8835b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8835b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8835b-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8835b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8835b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8835b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8835b-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8835b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8835b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8835b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8835b-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8835b-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8835b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8835b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8835b-126">MCI</span><span class="sxs-lookup"><span data-stu-id="8835b-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8835b-127">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="8835b-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





