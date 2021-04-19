---
description: Specifica informazioni su un documento associato a un'operazione di stampa DLP dell'endpoint.
title: DLP_PRINT_INFO struttura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495780"
---
# <a name="dlp_print_info-structure"></a><span data-ttu-id="dfa1d-103">DLP_PRINT_INFO struttura</span><span class="sxs-lookup"><span data-stu-id="dfa1d-103">DLP_PRINT_INFO structure</span></span>

<span data-ttu-id="dfa1d-104">Specifica informazioni su un documento associato a un'operazione di stampa DLP dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-104">Specifies information about a document that is associated with an endpoint DLP print operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa1d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfa1d-105">Syntax</span></span>


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a><span data-ttu-id="dfa1d-106">Members</span><span class="sxs-lookup"><span data-stu-id="dfa1d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dfa1d-107">*Versione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dfa1d-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa1d-108">Valore DWORD che specifica la versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="dfa1d-109">Questo valore deve essere sempre **DLP_PRINT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-109">This value should always be **DLP_PRINT_INFO_V_LATEST**.</span></span> <span data-ttu-id="dfa1d-110">Questa costante è definita nel file di intestazione di esempio endpointdlp.h nell'articolo [Prevenzione della perdita dei dati dell'endpoint](endpointdlp-endpoint-data-loss-prevention.md).</span><span class="sxs-lookup"><span data-stu-id="dfa1d-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="dfa1d-111">*PrinterName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dfa1d-111">*PrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa1d-112">Oggetto LPCWSTR che identifica la stampante di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-112">A LPCWSTR identifying the destination printer.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="dfa1d-113">*JobName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dfa1d-113">*JobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa1d-114">Oggetto LPCWSTR che specifica il nome del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-114">A LPCWSTR specifying print job name.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="dfa1d-115">*OutputFileName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dfa1d-115">*OutputFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa1d-116">Oggetto LPCWSTR che specifica il percorso del file di output, durante la stampa in un file.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-116">A LPCWSTR specifying the path to the output file, when printing to a file.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="dfa1d-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="dfa1d-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="dfa1d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfa1d-118">Requirements</span></span>



| <span data-ttu-id="dfa1d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa1d-119">Requirement</span></span>          |    <span data-ttu-id="dfa1d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dfa1d-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa1d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfa1d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa1d-122">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="dfa1d-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

