---
title: MCI_TMSF_TRACK macro (Mciapi. h)
description: La \_ macro MCI TMSF \_ Track Recupera il componente Tracks da un parametro contenente le informazioni sulle tracce compresse/minuti/secondi/frame (TMSF).
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873925"
---
# <a name="mci_tmsf_track-macro"></a><span data-ttu-id="00548-104">\_Macro di \_ rilevamento MCI TMSF</span><span class="sxs-lookup"><span data-stu-id="00548-104">MCI\_TMSF\_TRACK macro</span></span>

<span data-ttu-id="00548-105">La macro **MCI \_ TMSF \_ Track** Recupera il componente Tracks da un parametro contenente le informazioni sulle tracce compresse/minuti/secondi/frame (TMSF).</span><span class="sxs-lookup"><span data-stu-id="00548-105">The **MCI\_TMSF\_TRACK** macro retrieves the tracks component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="00548-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00548-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="00548-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="00548-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00548-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="00548-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="00548-109">Ora nel formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="00548-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00548-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00548-110">Return value</span></span>

<span data-ttu-id="00548-111">Restituisce il componente Tracks delle informazioni TMSF specificate.</span><span class="sxs-lookup"><span data-stu-id="00548-111">Returns the tracks component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="00548-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="00548-112">Remarks</span></span>

<span data-ttu-id="00548-113">L'ora nel formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente le tracce, il successivo byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il byte più significativo contenente i frame.</span><span class="sxs-lookup"><span data-stu-id="00548-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="00548-114">La macro **MCI \_ TMSF \_ Track** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="00548-114">The **MCI\_TMSF\_TRACK** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
```



## <a name="requirements"></a><span data-ttu-id="00548-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00548-115">Requirements</span></span>



| <span data-ttu-id="00548-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="00548-116">Requirement</span></span> | <span data-ttu-id="00548-117">Valore</span><span class="sxs-lookup"><span data-stu-id="00548-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00548-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00548-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00548-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00548-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00548-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00548-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00548-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00548-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00548-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00548-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00548-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="00548-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00548-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00548-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00548-125">MCI</span><span class="sxs-lookup"><span data-stu-id="00548-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="00548-126">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="00548-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





