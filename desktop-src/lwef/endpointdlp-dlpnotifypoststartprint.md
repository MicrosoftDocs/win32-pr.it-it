---
description: Fornisce al sistema informazioni su un documento dopo l'avvio di un'operazione di stampa.
title: Funzione DlpNotifyPostStartPrint (endpointdlp.h)
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
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495652"
---
# <a name="dlpnotifypoststartprint-function"></a><span data-ttu-id="3680b-103">Funzione DlpNotifyPostStartPrint</span><span class="sxs-lookup"><span data-stu-id="3680b-103">DlpNotifyPostStartPrint function</span></span>

<span data-ttu-id="3680b-104">Fornisce al sistema informazioni su un documento dopo l'avvio di un'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="3680b-104">Provides the system with information about a document after a print operation has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="3680b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3680b-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a><span data-ttu-id="3680b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3680b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3680b-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3680b-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3680b-108">Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento associato all'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="3680b-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3680b-109">*PrintInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3680b-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3680b-110">Puntatore a una [struttura DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenente informazioni sull'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="3680b-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="3680b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3680b-111">Return value</span></span>

<span data-ttu-id="3680b-112">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="3680b-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="3680b-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3680b-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="3680b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3680b-114">Requirements</span></span>



| <span data-ttu-id="3680b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3680b-115">Requirement</span></span>          |    <span data-ttu-id="3680b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3680b-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3680b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3680b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3680b-118">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="3680b-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="3680b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3680b-119">DLL</span></span><br/>                      | <span data-ttu-id="3680b-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="3680b-120">EndpointDlp.dll</span></span> |