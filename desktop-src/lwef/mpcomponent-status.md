---
title: Struttura MPCOMPONENT_STATUS (MpClient. h)
description: Informazioni sullo stato del componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- Struttura MPCOMPONENT_STATUS le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCOMPONENT_STATUS
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741023"
---
# <a name="mpcomponent_status-structure"></a><span data-ttu-id="711b7-105">\_Struttura di stato MPCOMPONENT</span><span class="sxs-lookup"><span data-stu-id="711b7-105">MPCOMPONENT\_STATUS structure</span></span>

<span data-ttu-id="711b7-106">Informazioni sullo stato del componente.</span><span class="sxs-lookup"><span data-stu-id="711b7-106">Component status information.</span></span>

## <a name="syntax"></a><span data-ttu-id="711b7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="711b7-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="711b7-108">Members</span><span class="sxs-lookup"><span data-stu-id="711b7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="711b7-109">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="711b7-109">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="711b7-110">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="711b7-110">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="711b7-111">Stato del componente.</span><span class="sxs-lookup"><span data-stu-id="711b7-111">Status for the component.</span></span>

</dd> <dt>

<span data-ttu-id="711b7-112">**hResult**</span><span class="sxs-lookup"><span data-stu-id="711b7-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="711b7-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="711b7-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="711b7-114">Codice di esito positivo o negativo associato allo stato.</span><span class="sxs-lookup"><span data-stu-id="711b7-114">Success or failure code associated with the status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="711b7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="711b7-115">Requirements</span></span>



| <span data-ttu-id="711b7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="711b7-116">Requirement</span></span> | <span data-ttu-id="711b7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="711b7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="711b7-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="711b7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="711b7-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="711b7-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="711b7-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="711b7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="711b7-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="711b7-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="711b7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="711b7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="711b7-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="711b7-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





