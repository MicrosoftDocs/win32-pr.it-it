---
title: Struttura MPTHREAT_INFOEX_UNUSED (MpClient. h)
description: Struttura fittizia per le minacce del tipo di modifica non del comportamento.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- Struttura MPTHREAT_INFOEX_UNUSED le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_INFOEX_UNUSED
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120342"
---
# <a name="mpthreat_infoex_unused-structure"></a><span data-ttu-id="83aeb-105">\_Struttura MPTHREAT INFOEX \_ inutilizzata</span><span class="sxs-lookup"><span data-stu-id="83aeb-105">MPTHREAT\_INFOEX\_UNUSED structure</span></span>

<span data-ttu-id="83aeb-106">Struttura fittizia per le minacce del tipo di modifica non del comportamento.</span><span class="sxs-lookup"><span data-stu-id="83aeb-106">Dummy structure for non-behavior modification type threats.</span></span>

## <a name="syntax"></a><span data-ttu-id="83aeb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83aeb-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="83aeb-108">Members</span><span class="sxs-lookup"><span data-stu-id="83aeb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="83aeb-109">**dwNone**</span><span class="sxs-lookup"><span data-stu-id="83aeb-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="83aeb-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="83aeb-110">Type: **DWORD**</span></span>

<span data-ttu-id="83aeb-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="83aeb-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="83aeb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83aeb-112">Requirements</span></span>



| <span data-ttu-id="83aeb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="83aeb-113">Requirement</span></span> | <span data-ttu-id="83aeb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="83aeb-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83aeb-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83aeb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="83aeb-116">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="83aeb-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="83aeb-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83aeb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="83aeb-118">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="83aeb-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83aeb-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83aeb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="83aeb-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="83aeb-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





