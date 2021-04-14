---
title: Enumerazione DODownloadState
description: Specifica l'ID dello stato di download corrente, che fa parte della struttura **DO_DOWNLOAD_STATUS** .
keywords:
- Enumerazione DODownloadState, DODownloadState
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518544"
---
# <a name="dodownloadstate-enumeration"></a><span data-ttu-id="bc012-104">Enumerazione DODownloadState</span><span class="sxs-lookup"><span data-stu-id="bc012-104">DODownloadState enumeration</span></span>

<span data-ttu-id="bc012-105">L'enumerazione **DODownloadState** specifica l'ID dello stato di download corrente, che fa parte della struttura **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="bc012-105">The **DODownloadState** enumeration specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc012-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc012-106">Syntax</span></span>

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a><span data-ttu-id="bc012-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="bc012-107">Constants</span></span>

| <span data-ttu-id="bc012-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc012-108">Requirement</span></span> | <span data-ttu-id="bc012-109">Valore</span><span class="sxs-lookup"><span data-stu-id="bc012-109">Value</span></span> |
|-|-|
| <span data-ttu-id="bc012-110">DODownloadState_Created</span><span class="sxs-lookup"><span data-stu-id="bc012-110">DODownloadState_Created</span></span> | <span data-ttu-id="bc012-111">L'oggetto di download è stato creato ma non è ancora stato avviato.</span><span class="sxs-lookup"><span data-stu-id="bc012-111">Download object is created but hasn't been started yet.</span></span> |
| <span data-ttu-id="bc012-112">DODownloadState_Transferring</span><span class="sxs-lookup"><span data-stu-id="bc012-112">DODownloadState_Transferring</span></span> | <span data-ttu-id="bc012-113">Il download è in corso.</span><span class="sxs-lookup"><span data-stu-id="bc012-113">Download is in progress.</span></span> |
| <span data-ttu-id="bc012-114">DODownloadState_Transferred</span><span class="sxs-lookup"><span data-stu-id="bc012-114">DODownloadState_Transferred</span></span> | <span data-ttu-id="bc012-115">Il download viene trasferito e può essere riavviato scaricando un'altra parte del file.</span><span class="sxs-lookup"><span data-stu-id="bc012-115">Download is transferred and can start again by downloading another portion of the file.</span></span> |
| <span data-ttu-id="bc012-116">DODownloadState_Finalized</span><span class="sxs-lookup"><span data-stu-id="bc012-116">DODownloadState_Finalized</span></span> | <span data-ttu-id="bc012-117">Il download è finalizzato e non può essere riavviato.</span><span class="sxs-lookup"><span data-stu-id="bc012-117">Download is finalized and cannot be started again.</span></span> |
| <span data-ttu-id="bc012-118">DODownloadState_Aborted</span><span class="sxs-lookup"><span data-stu-id="bc012-118">DODownloadState_Aborted</span></span> | <span data-ttu-id="bc012-119">Il download è stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="bc012-119">Download was aborted.</span></span> |
| <span data-ttu-id="bc012-120">DODownloadState_Paused</span><span class="sxs-lookup"><span data-stu-id="bc012-120">DODownloadState_Paused</span></span> | <span data-ttu-id="bc012-121">Il download è stato sospeso su richiesta o a causa di un errore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="bc012-121">Download has been paused on demand or due to transient error.</span></span> |

## <a name="requirements"></a><span data-ttu-id="bc012-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc012-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bc012-123">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="bc012-123">**Minimum supported client**</span></span> | <span data-ttu-id="bc012-124">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc012-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="bc012-125">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="bc012-125">**Minimum supported server**</span></span> | <span data-ttu-id="bc012-126">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="bc012-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="bc012-127">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="bc012-127">**Header**</span></span> | <span data-ttu-id="bc012-128">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="bc012-128">DeliveryOptimizationDownloadTypes.h</span></span> |
