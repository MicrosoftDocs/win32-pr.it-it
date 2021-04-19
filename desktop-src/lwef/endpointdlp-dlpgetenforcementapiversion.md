---
description: Recupera la versione dell'API prevenzione perdita dati (DLP) dell'endpoint nel dispositivo corrente.
title: Funzione DlpGetEnforcementApiVersion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495767"
---
# <a name="dlpgetenforcementapiversion-function"></a><span data-ttu-id="2b59a-103">Funzione DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="2b59a-103">DlpGetEnforcementApiVersion function</span></span>

<span data-ttu-id="2b59a-104">Recupera la versione dell'API prevenzione della perdita dei dati (DLP) dell'endpoint nel dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="2b59a-104">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b59a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b59a-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a><span data-ttu-id="2b59a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b59a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b59a-107">*MajorVersion* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2b59a-107">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b59a-108">Valore **DWORD che** specifica il numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="2b59a-108">A **DWORD** specifying the major version number.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="2b59a-109">*MajorVersion* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2b59a-109">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b59a-110">Valore **DWORD che** specifica il numero di versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="2b59a-110">A **DWORD** specifying the minor version number.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="2b59a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b59a-111">Return value</span></span>

<span data-ttu-id="2b59a-112">Restituisce un HRESULT che include, ma non solo, i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b59a-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="2b59a-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2b59a-113">HRESULT</span></span> | <span data-ttu-id="2b59a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b59a-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="2b59a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b59a-115">S_OK</span></span> | <span data-ttu-id="2b59a-116">La funzione è stata completata correttamente</span><span class="sxs-lookup"><span data-stu-id="2b59a-116">The function completed successfully</span></span> |




## <a name="remarks"></a><span data-ttu-id="2b59a-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="2b59a-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="2b59a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b59a-118">Requirements</span></span>



| <span data-ttu-id="2b59a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b59a-119">Requirement</span></span>          |    <span data-ttu-id="2b59a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2b59a-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b59a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b59a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b59a-122">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="2b59a-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="2b59a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2b59a-123">DLL</span></span><br/>                      | <span data-ttu-id="2b59a-124">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="2b59a-124">EndpointDlp.dll</span></span> |