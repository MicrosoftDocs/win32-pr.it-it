---
description: Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di salvataggio con nome.
title: Funzione DlpNotifyPreSaveAsDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495572"
---
# <a name="dlpnotifypresaveasdocument-function"></a><span data-ttu-id="bc2db-103">Funzione DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="bc2db-103">DlpNotifyPreSaveAsDocument function</span></span>

<span data-ttu-id="bc2db-104">Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di salvataggio con nome.</span><span class="sxs-lookup"><span data-stu-id="bc2db-104">Provides the system with information about a document before a save as operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc2db-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a><span data-ttu-id="bc2db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc2db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2db-107">*DocumentInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bc2db-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc2db-108">Puntatore a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenente informazioni sul documento da salvare.</span><span class="sxs-lookup"><span data-stu-id="bc2db-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="bc2db-109">*Destinazione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bc2db-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc2db-110">Oggetto **LPCWSTR** contenente il percorso di destinazione del documento da salvare.</span><span class="sxs-lookup"><span data-stu-id="bc2db-110">A **LPCWSTR** containing the destination path of the document to be saved.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="bc2db-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc2db-111">Return value</span></span>

<span data-ttu-id="bc2db-112">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="bc2db-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc2db-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bc2db-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="bc2db-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc2db-114">Requirements</span></span>



| <span data-ttu-id="bc2db-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc2db-115">Requirement</span></span>          |    <span data-ttu-id="bc2db-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bc2db-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2db-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc2db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bc2db-118">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="bc2db-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="bc2db-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bc2db-119">DLL</span></span><br/>                      | <span data-ttu-id="bc2db-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="bc2db-120">EndpointDlp.dll</span></span> |