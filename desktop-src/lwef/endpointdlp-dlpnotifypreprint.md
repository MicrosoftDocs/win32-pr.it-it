---
description: Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di stampa.
title: Funzione DlpNotifyPrePrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: eef5e3a19a6b93a49ba8b600be77385a99d3153a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495567"
---
# <a name="dlpnotifypreprint-function"></a><span data-ttu-id="7347f-103">Funzione DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="7347f-103">DlpNotifyPrePrint function</span></span>

<span data-ttu-id="7347f-104">Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="7347f-104">Provides the system with information about a document before a print operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7347f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7347f-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a><span data-ttu-id="7347f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7347f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7347f-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7347f-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7347f-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da stampare.</span><span class="sxs-lookup"><span data-stu-id="7347f-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be printed.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7347f-109">*PrintInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7347f-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7347f-110">Puntatore a una struttura [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenente informazioni sull'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="7347f-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="7347f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7347f-111">Return value</span></span>

<span data-ttu-id="7347f-112">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="7347f-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="7347f-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7347f-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="7347f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7347f-114">Requirements</span></span>



| <span data-ttu-id="7347f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7347f-115">Requirement</span></span>          |    <span data-ttu-id="7347f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7347f-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7347f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7347f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7347f-118">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="7347f-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="7347f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7347f-119">DLL</span></span><br/>                      | <span data-ttu-id="7347f-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="7347f-120">EndpointDlp.dll</span></span> |