---
title: Struttura MPTHREAT_DATA (MpClient. h)
description: Dati di notifica passati a causa di rilevamento o modifica delle minacce.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- Struttura MPTHREAT_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_DATA
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302652"
---
# <a name="mpthreat_data-structure"></a><span data-ttu-id="c2f53-105">\_Struttura dei dati MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="c2f53-105">MPTHREAT\_DATA structure</span></span>

<span data-ttu-id="c2f53-106">Dati di notifica passati a causa di rilevamento o modifica delle minacce.</span><span class="sxs-lookup"><span data-stu-id="c2f53-106">Notification data passed due to threat detection or modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f53-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2f53-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a><span data-ttu-id="c2f53-108">Members</span><span class="sxs-lookup"><span data-stu-id="c2f53-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2f53-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="c2f53-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="c2f53-110">Tipo: **MPTHREAT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c2f53-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="c2f53-111">Identificatore della minaccia.</span><span class="sxs-lookup"><span data-stu-id="c2f53-111">Threat identifier.</span></span> <span data-ttu-id="c2f53-112">Il bit superiore è impostato in modo da identificare le minacce correlate all'antivirus.</span><span class="sxs-lookup"><span data-stu-id="c2f53-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="c2f53-113">**dwSessionID**</span><span class="sxs-lookup"><span data-stu-id="c2f53-113">**dwSessionID**</span></span>
</dt> <dd>

<span data-ttu-id="c2f53-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c2f53-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c2f53-115">Sessione associata alla minaccia.</span><span class="sxs-lookup"><span data-stu-id="c2f53-115">Session associated with the threat.</span></span> <span data-ttu-id="c2f53-116">Impostare su-1 se non sono disponibili informazioni specifiche della sessione.</span><span class="sxs-lookup"><span data-stu-id="c2f53-116">Set to -1 if no session specific information is available.</span></span>

</dd> <dt>

<span data-ttu-id="c2f53-117">**ThreatAction**</span><span class="sxs-lookup"><span data-stu-id="c2f53-117">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="c2f53-118">Tipo: **[ **\_ azione MPTHREAT**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="c2f53-118">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c2f53-119">Si è tentato di eseguire un'azione di minaccia per gli eventi di pulizia della minaccia **MPNOTIFY \_ \_ \_ riuscita** / **MPNOTIFY \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c2f53-119">Threat action tried for the **MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**/**MPNOTIFY\_THREAT\_CLEAN\_FAILED** events.</span></span>

</dd> <dt>

<span data-ttu-id="c2f53-120">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="c2f53-120">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="c2f53-121">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c2f53-121">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c2f53-122">Stato o azioni aggiuntive associate all'azione eseguita.</span><span class="sxs-lookup"><span data-stu-id="c2f53-122">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="c2f53-123">Si tratta di una combinazione di flag di bit del [**\_ flag MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="c2f53-123">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2f53-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2f53-124">Requirements</span></span>



| <span data-ttu-id="c2f53-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f53-125">Requirement</span></span> | <span data-ttu-id="c2f53-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c2f53-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f53-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2f53-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f53-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c2f53-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c2f53-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2f53-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f53-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c2f53-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2f53-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2f53-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2f53-132"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2f53-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2f53-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2f53-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2f53-134">**\_flag MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="c2f53-134">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="c2f53-135">**\_azione MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c2f53-135">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





