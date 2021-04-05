---
title: MCI_TMSF_FRAME macro (Mciapi. h)
description: La \_ macro MCI TMSF \_ frame Recupera il componente frames da un parametro contenente le informazioni relative a tracce/minuti/secondi/frame (TMSF) compressi.
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740255"
---
# <a name="mci_tmsf_frame-macro"></a><span data-ttu-id="da55a-104">\_Macro TMSF \_ frame MCI</span><span class="sxs-lookup"><span data-stu-id="da55a-104">MCI\_TMSF\_FRAME macro</span></span>

<span data-ttu-id="da55a-105">La macro **MCI \_ TMSF \_ frame** Recupera il componente frames da un parametro contenente le informazioni relative a tracce/minuti/secondi/frame (TMSF) compressi.</span><span class="sxs-lookup"><span data-stu-id="da55a-105">The **MCI\_TMSF\_FRAME** macro retrieves the frames component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="da55a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da55a-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_FRAME(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="da55a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="da55a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da55a-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="da55a-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="da55a-109">Ora nel formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="da55a-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da55a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da55a-110">Return value</span></span>

<span data-ttu-id="da55a-111">Restituisce il componente frame delle informazioni TMSF specificate.</span><span class="sxs-lookup"><span data-stu-id="da55a-111">Returns the frames component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="da55a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="da55a-112">Remarks</span></span>

<span data-ttu-id="da55a-113">L'ora nel formato TMSF viene espressa come valore **DWORD** con il byte meno significativo contenente le tracce, il successivo byte meno significativo che contiene minuti, il successivo byte meno significativo contenente i secondi e il byte più significativo contenente i frame.</span><span class="sxs-lookup"><span data-stu-id="da55a-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="da55a-114">La **macro \_ TMSF \_ frame MCI** è definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="da55a-114">The **MCI\_TMSF\_FRAME** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
```



## <a name="requirements"></a><span data-ttu-id="da55a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da55a-115">Requirements</span></span>



| <span data-ttu-id="da55a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="da55a-116">Requirement</span></span> | <span data-ttu-id="da55a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="da55a-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da55a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da55a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da55a-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da55a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="da55a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da55a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="da55a-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da55a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="da55a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da55a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="da55a-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="da55a-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da55a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da55a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da55a-125">MCI</span><span class="sxs-lookup"><span data-stu-id="da55a-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="da55a-126">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="da55a-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





