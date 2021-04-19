---
description: Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di stampa.
title: Funzione DlpNotifyPostPrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495660"
---
# <a name="dlpnotifypostprint-function"></a><span data-ttu-id="65a69-103">Funzione DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="65a69-103">DlpNotifyPostPrint function</span></span>

<span data-ttu-id="65a69-104">Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="65a69-104">Provides the system with information about a document after a print operation has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65a69-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a><span data-ttu-id="65a69-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65a69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a69-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65a69-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a69-108">Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento associato all'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="65a69-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="65a69-109">*PrintInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65a69-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a69-110">Puntatore a una [struttura DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenente informazioni sull'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="65a69-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="65a69-111">*Stato operativo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65a69-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a69-112">Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato relative all'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="65a69-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="65a69-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65a69-113">Return value</span></span>

<span data-ttu-id="65a69-114">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="65a69-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a69-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="65a69-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="65a69-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65a69-116">Requirements</span></span>



| <span data-ttu-id="65a69-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65a69-117">Requirement</span></span>          |    <span data-ttu-id="65a69-118">Valore</span><span class="sxs-lookup"><span data-stu-id="65a69-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65a69-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65a69-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65a69-120">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="65a69-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="65a69-121">DLL</span><span class="sxs-lookup"><span data-stu-id="65a69-121">DLL</span></span><br/>                      | <span data-ttu-id="65a69-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="65a69-122">EndpointDlp.dll</span></span> |