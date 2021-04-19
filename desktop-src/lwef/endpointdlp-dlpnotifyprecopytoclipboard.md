---
description: Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di copia negli Appunti.
title: Funzione DlpNotifyPreCopyToClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b8e835e58d19570b9459d91ad131bbc0f38f378a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495644"
---
# <a name="dlpnotifyprecopytoclipboard-function"></a><span data-ttu-id="49403-103">Funzione DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="49403-103">DlpNotifyPreCopyToClipboard function</span></span>

<span data-ttu-id="49403-104">Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di copia negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="49403-104">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="49403-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49403-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="49403-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49403-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49403-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="49403-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49403-108">Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da cui viene copiato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="49403-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content is being copied.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="49403-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49403-109">Return value</span></span>

<span data-ttu-id="49403-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="49403-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="49403-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="49403-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="49403-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49403-112">Requirements</span></span>



| <span data-ttu-id="49403-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="49403-113">Requirement</span></span>          |    <span data-ttu-id="49403-114">Valore</span><span class="sxs-lookup"><span data-stu-id="49403-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49403-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49403-115">Minimum supported client</span></span><br/> | <span data-ttu-id="49403-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="49403-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="49403-117">DLL</span><span class="sxs-lookup"><span data-stu-id="49403-117">DLL</span></span><br/>                      | <span data-ttu-id="49403-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="49403-118">EndpointDlp.dll</span></span> |