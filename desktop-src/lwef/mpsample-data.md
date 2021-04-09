---
title: Struttura MPSAMPLE_DATA (MpClient. h)
description: Dati di notifica passati alla funzione di callback di invio dell'esempio.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- Struttura MPSAMPLE_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSAMPLE_DATA
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121515"
---
# <a name="mpsample_data-structure"></a><span data-ttu-id="2b327-105">\_Struttura dei dati MPSAMPLE</span><span class="sxs-lookup"><span data-stu-id="2b327-105">MPSAMPLE\_DATA structure</span></span>

<span data-ttu-id="2b327-106">Dati di notifica passati alla funzione di callback di invio dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="2b327-106">Notification data passed to the sample submission callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b327-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b327-107">Syntax</span></span>


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a><span data-ttu-id="2b327-108">Members</span><span class="sxs-lookup"><span data-stu-id="2b327-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b327-109">**dwSampleIndex**</span><span class="sxs-lookup"><span data-stu-id="2b327-109">**dwSampleIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2b327-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2b327-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2b327-111">Indice dell'elemento di esempio per il quale viene segnalato lo stato di invio.</span><span class="sxs-lookup"><span data-stu-id="2b327-111">Index of the sample item for which the submission status is reported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b327-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b327-112">Requirements</span></span>



| <span data-ttu-id="2b327-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b327-113">Requirement</span></span> | <span data-ttu-id="2b327-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2b327-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b327-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b327-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2b327-116">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2b327-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2b327-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b327-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2b327-118">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2b327-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b327-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b327-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b327-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b327-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





