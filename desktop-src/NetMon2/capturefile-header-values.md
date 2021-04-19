---
description: Definisce la struttura del file di intestazione Network Monitor.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Struttura CAPTUREFILE_HEADER_VALUES (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311638"
---
# <a name="capturefile_header_values-structure"></a><span data-ttu-id="b4052-103">\_ \_ Struttura dei valori dell'intestazione CAPTUREFILE</span><span class="sxs-lookup"><span data-stu-id="b4052-103">CAPTUREFILE\_HEADER\_VALUES structure</span></span>

<span data-ttu-id="b4052-104">La struttura dei **\_ \_ valori dell'intestazione CAPTUREFILE** definisce la struttura del file di intestazione Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="b4052-104">The **CAPTUREFILE\_HEADER\_VALUES** structure defines the Network Monitor header file structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4052-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4052-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a><span data-ttu-id="b4052-106">Members</span><span class="sxs-lookup"><span data-stu-id="b4052-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4052-107">**Firma**</span><span class="sxs-lookup"><span data-stu-id="b4052-107">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-108">Identificatore univoco:' GMBU.</span><span class="sxs-lookup"><span data-stu-id="b4052-108">Unique identifier: 'GMBU.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-109">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="b4052-109">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-110">Binario, decimale codificato (minore).</span><span class="sxs-lookup"><span data-stu-id="b4052-110">Binary, coded decimal (minor).</span></span> <span data-ttu-id="b4052-111">Il valore di questo membro deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="b4052-111">The value of this member should be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b4052-112">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="b4052-112">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-113">Decimal codificato binario (principale).</span><span class="sxs-lookup"><span data-stu-id="b4052-113">Binary coded decimal (major).</span></span> <span data-ttu-id="b4052-114">Questo valore deve essere 2.</span><span class="sxs-lookup"><span data-stu-id="b4052-114">This value should be 2.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="b4052-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-116">Tipo di topologia.</span><span class="sxs-lookup"><span data-stu-id="b4052-116">Topology type.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-117">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="b4052-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-118">Ora di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b4052-118">Time of capture.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-119">**FrameTableOffset**</span><span class="sxs-lookup"><span data-stu-id="b4052-119">**FrameTableOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-120">Tabella dell'indice del frame.</span><span class="sxs-lookup"><span data-stu-id="b4052-120">Frame index table.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-121">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="b4052-121">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-122">Dimensioni tabella indice frame.</span><span class="sxs-lookup"><span data-stu-id="b4052-122">Frame index table size.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-123">**UserDataOffset**</span><span class="sxs-lookup"><span data-stu-id="b4052-123">**UserDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-124">Offset dati utente.</span><span class="sxs-lookup"><span data-stu-id="b4052-124">User data offset.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-125">**UserDataLength**</span><span class="sxs-lookup"><span data-stu-id="b4052-125">**UserDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-126">Lunghezza dei dati utente.</span><span class="sxs-lookup"><span data-stu-id="b4052-126">User data length.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-127">**CommentDataOffset**</span><span class="sxs-lookup"><span data-stu-id="b4052-127">**CommentDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-128">Offset dei dati di commento.</span><span class="sxs-lookup"><span data-stu-id="b4052-128">Comment data offset.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-129">**CommentDataLength**</span><span class="sxs-lookup"><span data-stu-id="b4052-129">**CommentDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-130">Lunghezza dei dati di commento.</span><span class="sxs-lookup"><span data-stu-id="b4052-130">Length of comment data.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-131">**StatisticsOffset**</span><span class="sxs-lookup"><span data-stu-id="b4052-131">**StatisticsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-132">Offset alla struttura delle **statistiche** .</span><span class="sxs-lookup"><span data-stu-id="b4052-132">Offset to the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-133">**StatisticsLength**</span><span class="sxs-lookup"><span data-stu-id="b4052-133">**StatisticsLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-134">Lunghezza della struttura delle **statistiche** .</span><span class="sxs-lookup"><span data-stu-id="b4052-134">Length of the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-135">**NetworkInfoOffset**</span><span class="sxs-lookup"><span data-stu-id="b4052-135">**NetworkInfoOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-136">Offset alla struttura **NETWORKINFO** .</span><span class="sxs-lookup"><span data-stu-id="b4052-136">Offset to the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-137">**NetworkInfoLength**</span><span class="sxs-lookup"><span data-stu-id="b4052-137">**NetworkInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-138">Lunghezza della struttura **NETWORKINFO** .</span><span class="sxs-lookup"><span data-stu-id="b4052-138">Length of the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-139">**ConversationStatsOffset**</span><span class="sxs-lookup"><span data-stu-id="b4052-139">**ConversationStatsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-140">Questo membro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b4052-140">This member is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b4052-141">**ConversationStatsLength**</span><span class="sxs-lookup"><span data-stu-id="b4052-141">**ConversationStatsLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4052-142">Questo membro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b4052-142">This member is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4052-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4052-143">Requirements</span></span>



| <span data-ttu-id="b4052-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4052-144">Requirement</span></span> | <span data-ttu-id="b4052-145">Valore</span><span class="sxs-lookup"><span data-stu-id="b4052-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b4052-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4052-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b4052-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4052-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b4052-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4052-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b4052-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4052-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b4052-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4052-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4052-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4052-151"><dt>Netmon.h</dt></span></span> </dl> |



 

 




