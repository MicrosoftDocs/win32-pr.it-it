---
description: Fornisce al sistema informazioni su un file di documento al termine dell'operazione di apertura.
title: Funzione DlpNotifyPostOpenDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 0aed30cc0eca066b569ad1299392430c4d1adeff
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495687"
---
# <a name="dlpnotifypostopendocumentfile-function"></a><span data-ttu-id="8e2d0-103">Funzione DlpNotifyPostOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="8e2d0-103">DlpNotifyPostOpenDocumentFile function</span></span>

<span data-ttu-id="8e2d0-104">Fornisce al sistema informazioni su un file di documento dopo il completamento di un'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-104">Provides the system with information about a document file after an open operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e2d0-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus 
```

## <a name="parameters"></a><span data-ttu-id="8e2d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e2d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e2d0-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8e2d0-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e2d0-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento aperto.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="8e2d0-109">*OpStatus* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8e2d0-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e2d0-110">Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato dell'operazione di apertura del documento.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="8e2d0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e2d0-111">Return value</span></span>

<span data-ttu-id="8e2d0-112">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="8e2d0-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e2d0-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8e2d0-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="8e2d0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e2d0-114">Requirements</span></span>



| <span data-ttu-id="8e2d0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e2d0-115">Requirement</span></span>          |    <span data-ttu-id="8e2d0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8e2d0-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2d0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e2d0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e2d0-118">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="8e2d0-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="8e2d0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8e2d0-119">DLL</span></span><br/>                      | <span data-ttu-id="8e2d0-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="8e2d0-120">EndpointDlp.dll</span></span> |