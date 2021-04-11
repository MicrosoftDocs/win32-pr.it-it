---
title: MCI_TMSF_SECOND macro (Mciapi. h)
description: La \_ \_ seconda macro MCI TMSF Recupera il componente secondi da un parametro contenente le informazioni relative a tracce/minuti/secondi/frame (TMSF) compressi.
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722949487400f80ed72f9e120d5dbf8678ab81a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119990"
---
# <a name="mci_tmsf_second-macro"></a><span data-ttu-id="91526-104">\_TMSF \_ seconda macro MCI</span><span class="sxs-lookup"><span data-stu-id="91526-104">MCI\_TMSF\_SECOND macro</span></span>

<span data-ttu-id="91526-105">La **\_ \_ seconda macro MCI TMSF** Recupera il componente secondi da un parametro contenente le informazioni relative a tracce/minuti/secondi/frame (TMSF) compressi.</span><span class="sxs-lookup"><span data-stu-id="91526-105">The **MCI\_TMSF\_SECOND** macro retrieves the seconds component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="91526-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91526-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_SECOND(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="91526-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="91526-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91526-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="91526-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="91526-109">Ora nel formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="91526-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91526-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91526-110">Return value</span></span>

<span data-ttu-id="91526-111">Restituisce il componente relativo ai secondi delle informazioni TMSF specificate.</span><span class="sxs-lookup"><span data-stu-id="91526-111">Returns the seconds component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="91526-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="91526-112">Remarks</span></span>

<span data-ttu-id="91526-113">L'ora nel formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente le tracce, il successivo byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il byte più significativo contenente i frame.</span><span class="sxs-lookup"><span data-stu-id="91526-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="91526-114">La **\_ \_ seconda macro MCI TMSF** è definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="91526-114">The **MCI\_TMSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="91526-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91526-115">Requirements</span></span>



| <span data-ttu-id="91526-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="91526-116">Requirement</span></span> | <span data-ttu-id="91526-117">Valore</span><span class="sxs-lookup"><span data-stu-id="91526-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="91526-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91526-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91526-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91526-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="91526-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91526-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91526-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91526-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="91526-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91526-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91526-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="91526-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91526-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91526-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91526-125">MCI</span><span class="sxs-lookup"><span data-stu-id="91526-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="91526-126">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="91526-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





