---
description: Frame effettivo dal driver.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Struttura cornice (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305924"
---
# <a name="frame-structure"></a><span data-ttu-id="39e81-103">Struttura FRAME</span><span class="sxs-lookup"><span data-stu-id="39e81-103">FRAME structure</span></span>

<span data-ttu-id="39e81-104">La struttura del **frame** è un frame effettivo dal driver.</span><span class="sxs-lookup"><span data-stu-id="39e81-104">The **FRAME** structure is an actual frame from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e81-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39e81-105">Syntax</span></span>


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a><span data-ttu-id="39e81-106">Members</span><span class="sxs-lookup"><span data-stu-id="39e81-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="39e81-107">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="39e81-107">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="39e81-108">Tempo trascorso, in microsecondi, tra l'inizio dell'acquisizione e l'ora in cui è stato acquisito il frame.</span><span class="sxs-lookup"><span data-stu-id="39e81-108">Elapsed time, in microseconds, between the start of the capture and the time when the frame was captured.</span></span>

</dd> <dt>

<span data-ttu-id="39e81-109">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="39e81-109">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="39e81-110">Lunghezza del frame MAC.</span><span class="sxs-lookup"><span data-stu-id="39e81-110">MAC frame length.</span></span>

</dd> <dt>

<span data-ttu-id="39e81-111">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="39e81-111">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="39e81-112">Lunghezza effettiva del frame copiata.</span><span class="sxs-lookup"><span data-stu-id="39e81-112">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="39e81-113">**MacFrame**</span><span class="sxs-lookup"><span data-stu-id="39e81-113">**MacFrame**</span></span>
</dt> <dd>

<span data-ttu-id="39e81-114">Dati del frame.</span><span class="sxs-lookup"><span data-stu-id="39e81-114">Frame data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39e81-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39e81-115">Requirements</span></span>



| <span data-ttu-id="39e81-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e81-116">Requirement</span></span> | <span data-ttu-id="39e81-117">Valore</span><span class="sxs-lookup"><span data-stu-id="39e81-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39e81-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39e81-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39e81-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="39e81-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="39e81-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39e81-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39e81-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="39e81-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39e81-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39e81-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39e81-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="39e81-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




