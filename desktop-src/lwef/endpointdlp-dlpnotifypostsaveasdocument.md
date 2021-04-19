---
description: Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di salvataggio con nome.
title: Funzione DlpNotifyPostSaveAsDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495655"
---
# <a name="dlpnotifypostsaveasdocument-function"></a><span data-ttu-id="a40c2-103">Funzione DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="a40c2-103">DlpNotifyPostSaveAsDocument function</span></span>

<span data-ttu-id="a40c2-104">Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di salvataggio con nome.</span><span class="sxs-lookup"><span data-stu-id="a40c2-104">Provides the system with information about a document after the save as operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a40c2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a40c2-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="a40c2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a40c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a40c2-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a40c2-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a40c2-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento salvato.</span><span class="sxs-lookup"><span data-stu-id="a40c2-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a40c2-109">*Destinazione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a40c2-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a40c2-110">Oggetto **LPCWSTR** contenente il percorso di destinazione del documento salvato.</span><span class="sxs-lookup"><span data-stu-id="a40c2-110">A **LPCWSTR** containing the destination path the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a40c2-111">*OpStatus* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a40c2-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a40c2-112">Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato dell'operazione di salvataggio con nome.</span><span class="sxs-lookup"><span data-stu-id="a40c2-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the save as operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="a40c2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a40c2-113">Return value</span></span>

<span data-ttu-id="a40c2-114">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="a40c2-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="a40c2-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a40c2-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="a40c2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a40c2-116">Requirements</span></span>



| <span data-ttu-id="a40c2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a40c2-117">Requirement</span></span>          |    <span data-ttu-id="a40c2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a40c2-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a40c2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40c2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a40c2-120">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="a40c2-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="a40c2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a40c2-121">DLL</span></span><br/>                      | <span data-ttu-id="a40c2-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="a40c2-122">EndpointDlp.dll</span></span> |