---
title: Struttura MPRESERVED_DATA (MpClient. h)
description: Dati di notifica riservati.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- Struttura MPRESERVED_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPRESERVED_DATA
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120350"
---
# <a name="mpreserved_data-structure"></a><span data-ttu-id="72694-105">\_Struttura dei dati MPRESERVED</span><span class="sxs-lookup"><span data-stu-id="72694-105">MPRESERVED\_DATA structure</span></span>

<span data-ttu-id="72694-106">Dati di notifica riservati.</span><span class="sxs-lookup"><span data-stu-id="72694-106">Reserved notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="72694-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72694-107">Syntax</span></span>


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a><span data-ttu-id="72694-108">Members</span><span class="sxs-lookup"><span data-stu-id="72694-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="72694-109">**cbReservedData**</span><span class="sxs-lookup"><span data-stu-id="72694-109">**cbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="72694-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="72694-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="72694-111">Dimensioni in byte dei dati riservati.</span><span class="sxs-lookup"><span data-stu-id="72694-111">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="72694-112">**pbReservedData**</span><span class="sxs-lookup"><span data-stu-id="72694-112">**pbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="72694-113">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="72694-113">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="72694-114">Puntatore ai dati riservati.</span><span class="sxs-lookup"><span data-stu-id="72694-114">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72694-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72694-115">Requirements</span></span>



| <span data-ttu-id="72694-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72694-116">Requirement</span></span> | <span data-ttu-id="72694-117">Valore</span><span class="sxs-lookup"><span data-stu-id="72694-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72694-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72694-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72694-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="72694-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="72694-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72694-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72694-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="72694-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72694-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72694-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="72694-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="72694-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





