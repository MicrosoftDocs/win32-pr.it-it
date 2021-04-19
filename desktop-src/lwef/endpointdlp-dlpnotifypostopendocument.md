---
description: Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di apertura.
title: Funzione DlpNotifyPostOpenDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 10121e69ddbdc41516e56ec07e87a2f6dd8148cd
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495704"
---
# <a name="dlpnotifypostopendocument-function"></a><span data-ttu-id="b5137-103">Funzione DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="b5137-103">DlpNotifyPostOpenDocument function</span></span>

<span data-ttu-id="b5137-104">Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di apertura del documento.</span><span class="sxs-lookup"><span data-stu-id="b5137-104">Provides the system with information about a document after an open document operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5137-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5137-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="b5137-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5137-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b5137-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5137-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento aperto.</span><span class="sxs-lookup"><span data-stu-id="b5137-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b5137-109">*OpStatus* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b5137-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5137-110">Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato dell'operazione di apertura del documento.</span><span class="sxs-lookup"><span data-stu-id="b5137-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b5137-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5137-111">Return value</span></span>

<span data-ttu-id="b5137-112">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="b5137-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5137-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b5137-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b5137-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5137-114">Requirements</span></span>



| <span data-ttu-id="b5137-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5137-115">Requirement</span></span>          |    <span data-ttu-id="b5137-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b5137-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5137-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5137-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b5137-118">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="b5137-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b5137-119">DLL</span><span class="sxs-lookup"><span data-stu-id="b5137-119">DLL</span></span><br/>                      | <span data-ttu-id="b5137-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b5137-120">EndpointDlp.dll</span></span> |