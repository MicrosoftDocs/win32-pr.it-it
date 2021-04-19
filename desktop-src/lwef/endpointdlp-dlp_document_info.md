---
description: Specifica informazioni su un documento associato a un'operazione DLP dell'endpoint.
title: DLP_DOCUMENT_INFO struttura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495783"
---
# <a name="dlp_document_info-structure"></a><span data-ttu-id="46e37-103">DLP_DOCUMENT_INFO struttura</span><span class="sxs-lookup"><span data-stu-id="46e37-103">DLP_DOCUMENT_INFO structure</span></span>

<span data-ttu-id="46e37-104">Specifica informazioni su un documento associato a un'operazione DLP dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="46e37-104">Specifies information about a document that is associated with an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46e37-105">Syntax</span></span>


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a><span data-ttu-id="46e37-106">Members</span><span class="sxs-lookup"><span data-stu-id="46e37-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="46e37-107">*Versione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="46e37-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e37-108">Valore DWORD che specifica la versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="46e37-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="46e37-109">Questo valore deve essere sempre **DLP_DOCUMENT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="46e37-109">This value should always be **DLP_DOCUMENT_INFO_V_LATEST**.</span></span> <span data-ttu-id="46e37-110">Questa costante è definita nel file di intestazione di esempio endpointdlp.h nell'articolo [Prevenzione della perdita dei dati degli endpoint](endpointdlp-endpoint-data-loss-prevention.md).</span><span class="sxs-lookup"><span data-stu-id="46e37-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="46e37-111">*PersistentFileName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="46e37-111">*PersistentFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e37-112">Oggetto LPCWSTR che specifica il percorso originale del documento.</span><span class="sxs-lookup"><span data-stu-id="46e37-112">A LPCWSTR specifying the original path of the document.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="46e37-113">*LocalFileName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="46e37-113">*LocalFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e37-114">Oggetto LPCWSTR che specifica il percorso del file di backup reale del documento.</span><span class="sxs-lookup"><span data-stu-id="46e37-114">A LPCWSTR specifying the path to the real backing file of the document.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="46e37-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="46e37-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="46e37-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46e37-116">Requirements</span></span>



| <span data-ttu-id="46e37-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e37-117">Requirement</span></span>          |    <span data-ttu-id="46e37-118">Valore</span><span class="sxs-lookup"><span data-stu-id="46e37-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46e37-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46e37-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46e37-120">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="46e37-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

