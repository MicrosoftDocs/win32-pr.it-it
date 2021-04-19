---
description: Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di apertura.
title: Funzione DlpNotifyPreOpenDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 557554ad55a3a520fa95fcf53c8044881eed8b21
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495636"
---
# <a name="dlpnotifypreopendocument-function"></a><span data-ttu-id="deaf1-103">Funzione DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="deaf1-103">DlpNotifyPreOpenDocument function</span></span>

<span data-ttu-id="deaf1-104">Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="deaf1-104">Provides the system with information about a document before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="deaf1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="deaf1-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="deaf1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="deaf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deaf1-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="deaf1-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deaf1-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da aprire.</span><span class="sxs-lookup"><span data-stu-id="deaf1-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="deaf1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="deaf1-109">Return value</span></span>

<span data-ttu-id="deaf1-110">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="deaf1-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="deaf1-111">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="deaf1-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="deaf1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="deaf1-112">Requirements</span></span>



| <span data-ttu-id="deaf1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="deaf1-113">Requirement</span></span>          |    <span data-ttu-id="deaf1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="deaf1-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="deaf1-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="deaf1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="deaf1-116">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="deaf1-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="deaf1-117">DLL</span><span class="sxs-lookup"><span data-stu-id="deaf1-117">DLL</span></span><br/>                      | <span data-ttu-id="deaf1-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="deaf1-118">EndpointDlp.dll</span></span> |