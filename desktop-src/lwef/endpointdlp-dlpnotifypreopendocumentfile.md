---
description: Fornisce al sistema informazioni su un file di documento prima che venga avviata un'operazione di apertura.
title: Funzione DlpNotifyPreOpenDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 12caf5230d8affce195a63da155ed6b6ca409b72
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495631"
---
# <a name="dlpnotifypreopendocumentfile-function"></a><span data-ttu-id="095ab-103">Funzione DlpNotifyPreOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="095ab-103">DlpNotifyPreOpenDocumentFile function</span></span>

<span data-ttu-id="095ab-104">Fornisce al sistema informazioni su un file di documento prima che venga avviata un'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="095ab-104">Provides the system with information about a document file before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="095ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="095ab-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="095ab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="095ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="095ab-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="095ab-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095ab-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) struttura contenente informazioni sul documento da aprire.</span><span class="sxs-lookup"><span data-stu-id="095ab-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="095ab-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="095ab-109">Return value</span></span>

<span data-ttu-id="095ab-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="095ab-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="095ab-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="095ab-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="095ab-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="095ab-112">Requirements</span></span>



| <span data-ttu-id="095ab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="095ab-113">Requirement</span></span>          |    <span data-ttu-id="095ab-114">Valore</span><span class="sxs-lookup"><span data-stu-id="095ab-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="095ab-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="095ab-115">Minimum supported client</span></span><br/> | <span data-ttu-id="095ab-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="095ab-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="095ab-117">DLL</span><span class="sxs-lookup"><span data-stu-id="095ab-117">DLL</span></span><br/>                      | <span data-ttu-id="095ab-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="095ab-118">EndpointDlp.dll</span></span> |