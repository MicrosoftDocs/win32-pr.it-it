---
description: Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione Incolla dagli Appunti.
title: Funzione DlpNotifyPrePasteFromClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cfec6e7abbf2b94ce8bf78e0b1a10082ec54419d
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495559"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a><span data-ttu-id="2b776-103">Funzione DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="2b776-103">DlpNotifyPrePasteFromClipboard function</span></span>

<span data-ttu-id="2b776-104">Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione Incolla dagli Appunti.</span><span class="sxs-lookup"><span data-stu-id="2b776-104">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b776-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b776-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="2b776-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b776-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2b776-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b776-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento in cui viene incollato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="2b776-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content is being pasted.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="2b776-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b776-109">Return value</span></span>

<span data-ttu-id="2b776-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="2b776-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b776-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="2b776-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="2b776-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b776-112">Requirements</span></span>



| <span data-ttu-id="2b776-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b776-113">Requirement</span></span>          |    <span data-ttu-id="2b776-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2b776-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b776-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b776-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2b776-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="2b776-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="2b776-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2b776-117">DLL</span></span><br/>                      | <span data-ttu-id="2b776-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="2b776-118">EndpointDlp.dll</span></span> |