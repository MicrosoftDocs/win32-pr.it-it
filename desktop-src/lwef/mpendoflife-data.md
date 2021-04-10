---
title: Struttura MPENDOFLIFE_DATA (MpClient. h)
description: '\ 0034; Fine vita \ 0034; dati di notifica.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- Struttura MPENDOFLIFE_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPENDOFLIFE_DATA
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120551"
---
# <a name="mpendoflife_data-structure"></a><span data-ttu-id="3e88d-105">\_Struttura dei dati MPENDOFLIFE</span><span class="sxs-lookup"><span data-stu-id="3e88d-105">MPENDOFLIFE\_DATA structure</span></span>

<span data-ttu-id="3e88d-106">Dati di notifica di "fine vita".</span><span class="sxs-lookup"><span data-stu-id="3e88d-106">"End of life" notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e88d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e88d-107">Syntax</span></span>


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a><span data-ttu-id="3e88d-108">Members</span><span class="sxs-lookup"><span data-stu-id="3e88d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e88d-109">**ftSignatureExpiry**</span><span class="sxs-lookup"><span data-stu-id="3e88d-109">**ftSignatureExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="3e88d-110">Tipo: **FILEtime**</span><span class="sxs-lookup"><span data-stu-id="3e88d-110">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="3e88d-111">Ora di scadenza della firma.</span><span class="sxs-lookup"><span data-stu-id="3e88d-111">Time when the signature expires.</span></span>

</dd> <dt>

<span data-ttu-id="3e88d-112">**ftPlatformExpiry**</span><span class="sxs-lookup"><span data-stu-id="3e88d-112">**ftPlatformExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="3e88d-113">Tipo: **FILEtime**</span><span class="sxs-lookup"><span data-stu-id="3e88d-113">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="3e88d-114">Ora di scadenza della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="3e88d-114">Time when the platform expires.</span></span>

</dd> <dt>

<span data-ttu-id="3e88d-115">**fAdminControlled**</span><span class="sxs-lookup"><span data-stu-id="3e88d-115">**fAdminControlled**</span></span>
</dt> <dd>

<span data-ttu-id="3e88d-116">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="3e88d-116">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="3e88d-117">True se l'amministratore controlla i criteri per la visualizzazione della notifica.</span><span class="sxs-lookup"><span data-stu-id="3e88d-117">True if the administrator controlling the policy for showing the notification.</span></span> <span data-ttu-id="3e88d-118">Se impostato, indica all'interfaccia utente di non visualizzare la notifica EOL.</span><span class="sxs-lookup"><span data-stu-id="3e88d-118">If set, this tells the UI to not show the EOL notification.</span></span>

</dd> <dt>

<span data-ttu-id="3e88d-119">**fEndOfLifeImpendingOrPast**</span><span class="sxs-lookup"><span data-stu-id="3e88d-119">**fEndOfLifeImpendingOrPast**</span></span>
</dt> <dd>

<span data-ttu-id="3e88d-120">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="3e88d-120">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="3e88d-121">True se "End of Life" è in sospeso o passato.</span><span class="sxs-lookup"><span data-stu-id="3e88d-121">True if "End of Life" is pending or past.</span></span> <span data-ttu-id="3e88d-122">Se false, l'interfaccia utente e i client possono cancellare tutti gli stati correlati a EOL.</span><span class="sxs-lookup"><span data-stu-id="3e88d-122">If false, UI and clients can clear any EOL related states.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e88d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e88d-123">Requirements</span></span>



| <span data-ttu-id="3e88d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e88d-124">Requirement</span></span> | <span data-ttu-id="3e88d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3e88d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e88d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e88d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e88d-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3e88d-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3e88d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e88d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e88d-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3e88d-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e88d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e88d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e88d-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e88d-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





