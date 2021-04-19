---
description: Fornisce al sistema informazioni su un documento quando viene immessa una destinazione di rilascio.
title: Funzione DlpNotifyEnterDropTarget (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ec1eee1cee7bbcc38ce3094e3e2f8b650cf3b2a9
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495713"
---
# <a name="dlpnotifyenterdroptarget-function"></a><span data-ttu-id="16785-103">Funzione DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="16785-103">DlpNotifyEnterDropTarget function</span></span>

<span data-ttu-id="16785-104">Fornisce al sistema informazioni su un documento quando viene immessa una destinazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="16785-104">Provides the system with information about a document when a drop target is entered.</span></span>

## <a name="syntax"></a><span data-ttu-id="16785-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16785-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="16785-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16785-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16785-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="16785-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16785-108">Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento associato all'operazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="16785-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="16785-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16785-109">Return value</span></span>

<span data-ttu-id="16785-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="16785-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="16785-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="16785-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="16785-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16785-112">Requirements</span></span>



| <span data-ttu-id="16785-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="16785-113">Requirement</span></span>          |    <span data-ttu-id="16785-114">Valore</span><span class="sxs-lookup"><span data-stu-id="16785-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16785-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16785-115">Minimum supported client</span></span><br/> | <span data-ttu-id="16785-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="16785-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="16785-117">DLL</span><span class="sxs-lookup"><span data-stu-id="16785-117">DLL</span></span><br/>                      | <span data-ttu-id="16785-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="16785-118">EndpointDlp.dll</span></span> |