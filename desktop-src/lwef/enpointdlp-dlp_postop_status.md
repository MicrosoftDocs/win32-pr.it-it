---
description: Specifica le informazioni sullo stato di un'operazione DLP dell'endpoint.
title: DLP_POSTOP_STATUS struttura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495580"
---
# <a name="dlp_postop_status-structure"></a><span data-ttu-id="176ae-103">DLP_POSTOP_STATUS struttura</span><span class="sxs-lookup"><span data-stu-id="176ae-103">DLP_POSTOP_STATUS structure</span></span>

<span data-ttu-id="176ae-104">Specifica le informazioni sullo stato di un'operazione DLP dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="176ae-104">Specifies status information about an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="176ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="176ae-105">Syntax</span></span>


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a><span data-ttu-id="176ae-106">Members</span><span class="sxs-lookup"><span data-stu-id="176ae-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="176ae-107">*Versione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="176ae-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="176ae-108">Valore DWORD che specifica la versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="176ae-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="176ae-109">Questo valore deve essere sempre **DLP_POSTOP_STATUS_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="176ae-109">This value should always be **DLP_POSTOP_STATUS_V_LATEST**.</span></span> <span data-ttu-id="176ae-110">Questa costante è definita nel file di intestazione di esempio endpointdlp.h nell'articolo [Prevenzione della perdita dei dati degli endpoint](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="176ae-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md)</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="176ae-111">*OperazioneSuccess* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="176ae-111">*OperationSuccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="176ae-112">Valore BOOL che indica se l'operazione di apertura è riuscita.</span><span class="sxs-lookup"><span data-stu-id="176ae-112">A BOOL indicating whether the open operation was successful.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="176ae-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="176ae-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="176ae-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="176ae-114">Requirements</span></span>



| <span data-ttu-id="176ae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="176ae-115">Requirement</span></span>          |    <span data-ttu-id="176ae-116">Valore</span><span class="sxs-lookup"><span data-stu-id="176ae-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="176ae-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="176ae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="176ae-118">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="176ae-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
