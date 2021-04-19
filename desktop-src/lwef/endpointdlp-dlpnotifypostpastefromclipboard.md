---
description: Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione Incolla dagli Appunti.
title: Funzione DlpNotifyPostPasteFromClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 69a5afbc41350092ebd4d433d2f4d7259ece82cf
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495663"
---
# <a name="dlpnotifypostpastefromclipboard-function"></a><span data-ttu-id="26d93-103">Funzione DlpNotifyPostPasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="26d93-103">DlpNotifyPostPasteFromClipboard function</span></span>

<span data-ttu-id="26d93-104">Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione Incolla dagli Appunti.</span><span class="sxs-lookup"><span data-stu-id="26d93-104">Provides the system with information about a document after a paste from clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d93-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26d93-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="26d93-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26d93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d93-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="26d93-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d93-108">Puntatore a una [struttura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento in cui è stato copiato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="26d93-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="26d93-109">*Stato operativo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="26d93-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d93-110">Puntatore a una struttura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenente informazioni sullo stato relative all'operazione Incolla dagli Appunti.</span><span class="sxs-lookup"><span data-stu-id="26d93-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the paste from clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="26d93-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26d93-111">Return value</span></span>

<span data-ttu-id="26d93-112">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="26d93-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d93-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="26d93-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="26d93-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26d93-114">Requirements</span></span>



| <span data-ttu-id="26d93-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d93-115">Requirement</span></span>          |    <span data-ttu-id="26d93-116">Valore</span><span class="sxs-lookup"><span data-stu-id="26d93-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26d93-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26d93-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26d93-118">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="26d93-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="26d93-119">DLL</span><span class="sxs-lookup"><span data-stu-id="26d93-119">DLL</span></span><br/>                      | <span data-ttu-id="26d93-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="26d93-120">EndpointDlp.dll</span></span> |