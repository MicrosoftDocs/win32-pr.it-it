---
description: Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di trascinamento della selezione.
title: Funzione DlpNotifyPreDragDrop (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d88a28c0dff4b13cf1c1848eeb8623c3acd1c024
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495639"
---
# <a name="dlpnotifypredragdrop-function"></a><span data-ttu-id="c35db-103">Funzione DlpNotifyPreDragDrop</span><span class="sxs-lookup"><span data-stu-id="c35db-103">DlpNotifyPreDragDrop function</span></span>

<span data-ttu-id="c35db-104">Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="c35db-104">Provides the system with information about a document before a drag drop operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c35db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c35db-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="c35db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c35db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c35db-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c35db-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c35db-108">Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento associato all'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="c35db-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="c35db-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c35db-109">Return value</span></span>

<span data-ttu-id="c35db-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="c35db-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="c35db-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c35db-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c35db-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c35db-112">Requirements</span></span>



| <span data-ttu-id="c35db-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c35db-113">Requirement</span></span>          |    <span data-ttu-id="c35db-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c35db-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c35db-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c35db-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c35db-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="c35db-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="c35db-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c35db-117">DLL</span></span><br/>                      | <span data-ttu-id="c35db-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="c35db-118">EndpointDlp.dll</span></span> |