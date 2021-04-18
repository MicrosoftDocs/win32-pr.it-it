---
description: La \_ struttura del descrittore di frame fornisce informazioni descrittive sui frame non elaborati.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Struttura FRAME_DESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305926"
---
# <a name="frame_descriptor-structure"></a><span data-ttu-id="b9a99-103">\_Struttura del descrittore di frame</span><span class="sxs-lookup"><span data-stu-id="b9a99-103">FRAME\_DESCRIPTOR structure</span></span>

<span data-ttu-id="b9a99-104">La struttura del **\_ descrittore di frame** fornisce informazioni descrittive sui frame non elaborati.</span><span class="sxs-lookup"><span data-stu-id="b9a99-104">The **FRAME\_DESCRIPTOR** structure provides descriptive information about raw frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a99-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9a99-105">Syntax</span></span>


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="b9a99-106">Members</span><span class="sxs-lookup"><span data-stu-id="b9a99-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9a99-107">**FramePointer**</span><span class="sxs-lookup"><span data-stu-id="b9a99-107">**FramePointer**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-108">Puntatore ai dati del frame.</span><span class="sxs-lookup"><span data-stu-id="b9a99-108">Pointer to frame data.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-109">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="b9a99-109">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-110">Tempo di sistema, in microsecondi, quando il frame è stato acquisito.</span><span class="sxs-lookup"><span data-stu-id="b9a99-110">System time, in microseconds, when the frame was captured.</span></span> <span data-ttu-id="b9a99-111">Questo tempo viene in genere usato per determinare l'intervallo tra l'acquisizione di due frame.</span><span class="sxs-lookup"><span data-stu-id="b9a99-111">This time is typically used to determine the interval between the times two frames were captured.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-112">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="b9a99-112">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-113">Lunghezza del frame.</span><span class="sxs-lookup"><span data-stu-id="b9a99-113">Length of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-114">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="b9a99-114">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-115">Lunghezza effettiva del frame copiata.</span><span class="sxs-lookup"><span data-stu-id="b9a99-115">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-116">**Etype**</span><span class="sxs-lookup"><span data-stu-id="b9a99-116">**Etype**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-117">Nome etype.</span><span class="sxs-lookup"><span data-stu-id="b9a99-117">Etype name.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-118">**SAP**</span><span class="sxs-lookup"><span data-stu-id="b9a99-118">**Sap**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-119">Valore SAP.</span><span class="sxs-lookup"><span data-stu-id="b9a99-119">SAP value.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-120">**LowProtocol**</span><span class="sxs-lookup"><span data-stu-id="b9a99-120">**LowProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-121">Indice del protocollo trovato.</span><span class="sxs-lookup"><span data-stu-id="b9a99-121">Index of protocol found.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-122">**LowProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="b9a99-122">**LowProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-123">Offset ai dati del protocollo ottenuti da **LowProtocol**.</span><span class="sxs-lookup"><span data-stu-id="b9a99-123">Offset to protocol data obtained from **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-124">**HighPort**</span><span class="sxs-lookup"><span data-stu-id="b9a99-124">**HighPort**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-125">Porta del protocollo elevato identificato in **LowProtocol**.</span><span class="sxs-lookup"><span data-stu-id="b9a99-125">Port of high protocol identified in **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="b9a99-126">**HighProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="b9a99-126">**HighProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b9a99-127">Offset ai dati del protocollo ottenuti da **HighPort**.</span><span class="sxs-lookup"><span data-stu-id="b9a99-127">Offset to protocol data obtained from **HighPort**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9a99-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9a99-128">Requirements</span></span>



| <span data-ttu-id="b9a99-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9a99-129">Requirement</span></span> | <span data-ttu-id="b9a99-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b9a99-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a99-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9a99-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a99-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9a99-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b9a99-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9a99-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a99-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9a99-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b9a99-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9a99-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9a99-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9a99-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




