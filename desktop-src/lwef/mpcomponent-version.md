---
title: Struttura MPCOMPONENT_VERSION (MpClient. h)
description: Tempo di aggiornamento e versione per un singolo componente.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- Struttura MPCOMPONENT_VERSION le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCOMPONENT_VERSION
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964166"
---
# <a name="mpcomponent_version-structure"></a><span data-ttu-id="3ec44-105">Struttura della versione di MPCOMPONENT \_</span><span class="sxs-lookup"><span data-stu-id="3ec44-105">MPCOMPONENT\_VERSION structure</span></span>

<span data-ttu-id="3ec44-106">Tempo di aggiornamento e versione per un singolo componente.</span><span class="sxs-lookup"><span data-stu-id="3ec44-106">Version and update time for an individual component.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec44-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ec44-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a><span data-ttu-id="3ec44-108">Members</span><span class="sxs-lookup"><span data-stu-id="3ec44-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ec44-109">**Versione**</span><span class="sxs-lookup"><span data-stu-id="3ec44-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="3ec44-110">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="3ec44-110">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="3ec44-111">Campo della versione.</span><span class="sxs-lookup"><span data-stu-id="3ec44-111">Version field.</span></span> <span data-ttu-id="3ec44-112">Ogni **parola** rappresenta Major, minor, Build e Revision.</span><span class="sxs-lookup"><span data-stu-id="3ec44-112">Each **WORD** represents major, minor, build, and revision.</span></span>

</dd> <dt>

<span data-ttu-id="3ec44-113">**UpdateTime**</span><span class="sxs-lookup"><span data-stu-id="3ec44-113">**UpdateTime**</span></span>
</dt> <dd>

<span data-ttu-id="3ec44-114">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="3ec44-114">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="3ec44-115">Ora dell'ultimo aggiornamento del componente, nel formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="3ec44-115">Last update time of the component, in **FILETIME** format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ec44-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ec44-116">Requirements</span></span>



| <span data-ttu-id="3ec44-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ec44-117">Requirement</span></span> | <span data-ttu-id="3ec44-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3ec44-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec44-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ec44-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec44-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3ec44-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3ec44-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ec44-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec44-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3ec44-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ec44-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ec44-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec44-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ec44-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





