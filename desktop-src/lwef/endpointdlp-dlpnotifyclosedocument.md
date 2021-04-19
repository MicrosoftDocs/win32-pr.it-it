---
description: Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di chiusura del documento.
title: Funzione DlpNotifyCloseDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 06c2b2527833b498ab2b7f5f3fa0f5a662fe67d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495722"
---
# <a name="dlpnotifyclosedocument-function"></a><span data-ttu-id="b3c97-103">Funzione DlpNotifyCloseDocument</span><span class="sxs-lookup"><span data-stu-id="b3c97-103">DlpNotifyCloseDocument function</span></span>

<span data-ttu-id="b3c97-104">Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di chiusura del documento.</span><span class="sxs-lookup"><span data-stu-id="b3c97-104">Provides the system with information about a document before the document close operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3c97-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="b3c97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3c97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c97-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b3c97-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c97-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da aprire.</span><span class="sxs-lookup"><span data-stu-id="b3c97-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b3c97-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3c97-109">Return value</span></span>

<span data-ttu-id="b3c97-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="b3c97-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c97-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b3c97-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b3c97-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3c97-112">Requirements</span></span>



| <span data-ttu-id="b3c97-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c97-113">Requirement</span></span>          |    <span data-ttu-id="b3c97-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b3c97-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c97-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3c97-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c97-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="b3c97-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b3c97-117">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c97-117">DLL</span></span><br/>                      | <span data-ttu-id="b3c97-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b3c97-118">EndpointDlp.dll</span></span> |