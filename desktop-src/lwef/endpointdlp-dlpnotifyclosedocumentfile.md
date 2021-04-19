---
description: Fornisce al sistema informazioni su un documento prima che venga avviata l'operazione di chiusura del file del documento.
title: Funzione DlpNotifyCloseDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2438829cde84e9029a86d74e4ed704e1e8d33511
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495719"
---
# <a name="dlpnotifyclosedocumentfile-function"></a><span data-ttu-id="46eae-103">Funzione DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="46eae-103">DlpNotifyCloseDocumentFile function</span></span>

<span data-ttu-id="46eae-104">Fornisce al sistema informazioni su un documento prima che venga avviata l'operazione di chiusura del file del documento.</span><span class="sxs-lookup"><span data-stu-id="46eae-104">Provides the system with information about a document before the document file close operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="46eae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46eae-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="46eae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46eae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46eae-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="46eae-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46eae-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) struttura contenente informazioni sul documento da aprire.</span><span class="sxs-lookup"><span data-stu-id="46eae-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="46eae-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46eae-109">Return value</span></span>

<span data-ttu-id="46eae-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="46eae-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="46eae-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="46eae-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="46eae-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46eae-112">Requirements</span></span>


| <span data-ttu-id="46eae-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="46eae-113">Requirement</span></span>          |    <span data-ttu-id="46eae-114">Valore</span><span class="sxs-lookup"><span data-stu-id="46eae-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46eae-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46eae-115">Minimum supported client</span></span><br/> | <span data-ttu-id="46eae-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="46eae-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="46eae-117">DLL</span><span class="sxs-lookup"><span data-stu-id="46eae-117">DLL</span></span><br/>                      | <span data-ttu-id="46eae-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="46eae-118">EndpointDlp.dll</span></span> |