---
description: Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di copia negli Appunti.
title: Funzione DlpNotifyPostCopyToClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b4b1a375d68819fc36f82a530a7fe7a8abe881c0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495710"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a><span data-ttu-id="17808-103">Funzione DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="17808-103">DlpNotifyPostCopyToClipboard function</span></span>

<span data-ttu-id="17808-104">Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di copia negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="17808-104">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="17808-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17808-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="17808-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17808-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17808-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17808-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17808-108">Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da cui è stato copiato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="17808-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="17808-109">*OpStatus* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17808-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17808-110">Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato dell'operazione di copia negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="17808-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the copy to clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="17808-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17808-111">Return value</span></span>

<span data-ttu-id="17808-112">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="17808-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="17808-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="17808-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="17808-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17808-114">Requirements</span></span>



| <span data-ttu-id="17808-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="17808-115">Requirement</span></span>          |    <span data-ttu-id="17808-116">Valore</span><span class="sxs-lookup"><span data-stu-id="17808-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17808-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17808-117">Minimum supported client</span></span><br/> | <span data-ttu-id="17808-118">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="17808-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="17808-119">DLL</span><span class="sxs-lookup"><span data-stu-id="17808-119">DLL</span></span><br/>                      | <span data-ttu-id="17808-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="17808-120">EndpointDlp.dll</span></span> |