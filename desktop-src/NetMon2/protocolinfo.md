---
description: La struttura PROTOCOLINFO descrive un protocollo.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Struttura PROTOCOLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315452"
---
# <a name="protocolinfo-structure"></a><span data-ttu-id="ec185-103">Struttura PROTOCOLINFO</span><span class="sxs-lookup"><span data-stu-id="ec185-103">PROTOCOLINFO structure</span></span>

<span data-ttu-id="ec185-104">La struttura **PROTOCOLINFO** descrive un protocollo.</span><span class="sxs-lookup"><span data-stu-id="ec185-104">The **PROTOCOLINFO** structure describes a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec185-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec185-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a><span data-ttu-id="ec185-106">Members</span><span class="sxs-lookup"><span data-stu-id="ec185-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec185-107">**ProtocolID**</span><span class="sxs-lookup"><span data-stu-id="ec185-107">**ProtocolID**</span></span>
</dt> <dd>

<span data-ttu-id="ec185-108">Identificatore di protocollo assegnato dal sistema della sessione di esecuzione specificata.</span><span class="sxs-lookup"><span data-stu-id="ec185-108">System-assigned protocol identifier of the specified run session.</span></span>

</dd> <dt>

<span data-ttu-id="ec185-109">**PropertyDatabase**</span><span class="sxs-lookup"><span data-stu-id="ec185-109">**PropertyDatabase**</span></span>
</dt> <dd>

<span data-ttu-id="ec185-110">Database di proprietà del protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="ec185-110">Property database of the specified protocol.</span></span>

</dd> <dt>

<span data-ttu-id="ec185-111">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="ec185-111">**ProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="ec185-112">Nome del protocollo abbreviato.</span><span class="sxs-lookup"><span data-stu-id="ec185-112">Abbreviated protocol name.</span></span>

</dd> <dt>

<span data-ttu-id="ec185-113">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="ec185-113">**HelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="ec185-114">Nome del file della guida facoltativo associato al protocollo.</span><span class="sxs-lookup"><span data-stu-id="ec185-114">Optional Help file name associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="ec185-115">**Commento**</span><span class="sxs-lookup"><span data-stu-id="ec185-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="ec185-116">Commento che descrive il protocollo.</span><span class="sxs-lookup"><span data-stu-id="ec185-116">A comment describing the protocol.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec185-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec185-117">Requirements</span></span>



| <span data-ttu-id="ec185-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec185-118">Requirement</span></span> | <span data-ttu-id="ec185-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ec185-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ec185-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec185-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ec185-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ec185-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ec185-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec185-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ec185-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ec185-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ec185-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec185-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec185-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec185-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




