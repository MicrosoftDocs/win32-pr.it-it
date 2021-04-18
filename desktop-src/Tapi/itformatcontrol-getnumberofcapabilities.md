---
description: Il metodo GetNumberOfCapabilities Recupera il numero di funzionalità associate al formato corrente.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'Metodo ITFormatControl:: GetNumberOfCapabilities (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329459"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a><span data-ttu-id="5d908-103">Metodo ITFormatControl:: GetNumberOfCapabilities</span><span class="sxs-lookup"><span data-stu-id="5d908-103">ITFormatControl::GetNumberOfCapabilities method</span></span>

<span data-ttu-id="5d908-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5d908-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5d908-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="5d908-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5d908-106">Il metodo **GetNumberOfCapabilities** Recupera il numero di funzionalità associate al formato corrente.</span><span class="sxs-lookup"><span data-stu-id="5d908-106">The **GetNumberOfCapabilities** method retrieves the number of capabilities associated with the current format.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d908-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d908-107">Syntax</span></span>


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a><span data-ttu-id="5d908-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d908-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d908-109">*pdwCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5d908-109">*pdwCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d908-110">Conteggio delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5d908-110">Count of the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d908-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d908-111">Return value</span></span>

<span data-ttu-id="5d908-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="5d908-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5d908-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5d908-113">Return code</span></span>                                                                                   | <span data-ttu-id="5d908-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d908-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5d908-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5d908-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5d908-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5d908-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5d908-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="5d908-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5d908-118">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5d908-118">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d908-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d908-119">Requirements</span></span>



| <span data-ttu-id="5d908-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d908-120">Requirement</span></span> | <span data-ttu-id="5d908-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5d908-121">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d908-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5d908-122">TAPI version</span></span><br/> | <span data-ttu-id="5d908-123">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="5d908-123">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="5d908-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d908-124">Header</span></span><br/>       | <dl> <span data-ttu-id="5d908-125"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d908-125"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d908-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5d908-126">Library</span></span><br/>      | <dl> <span data-ttu-id="5d908-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d908-127"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="5d908-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5d908-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="5d908-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d908-129"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d908-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d908-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d908-131">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="5d908-131">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




