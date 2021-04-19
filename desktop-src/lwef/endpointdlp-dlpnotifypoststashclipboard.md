---
description: Fornisce al sistema informazioni sullo stato dopo il completamento di un'operazione di stash degli Appunti.
title: Funzione DlpNotifyPostStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495647"
---
# <a name="dlpnotifypoststashclipboard-function"></a><span data-ttu-id="c69ce-103">Funzione DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="c69ce-103">DlpNotifyPostStashClipboard function</span></span>

<span data-ttu-id="c69ce-104">Fornisce al sistema informazioni sullo stato dopo il completamento di un'operazione di stash degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="c69ce-104">Provides the system with status information after a stash clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69ce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c69ce-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="c69ce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c69ce-106">Parameters</span></span>


<dl> <dt>

<span data-ttu-id="c69ce-107">*OpStatus* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c69ce-107">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c69ce-108">Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato dell'operazione stash clipboard.</span><span class="sxs-lookup"><span data-stu-id="c69ce-108">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the stash clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="c69ce-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c69ce-109">Return value</span></span>

<span data-ttu-id="c69ce-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="c69ce-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="c69ce-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c69ce-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c69ce-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c69ce-112">Requirements</span></span>



| <span data-ttu-id="c69ce-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c69ce-113">Requirement</span></span>          |    <span data-ttu-id="c69ce-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c69ce-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c69ce-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c69ce-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c69ce-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="c69ce-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="c69ce-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c69ce-117">DLL</span></span><br/>                      | <span data-ttu-id="c69ce-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="c69ce-118">EndpointDlp.dll</span></span> |