---
description: 'Metodo IEnumMedia::Skip: il metodo Skip ignora il successivo numero specificato di elementi nella sequenza di enumerazione.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: Metodo IEnumMedia::Skip (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8c600a201d6800fcb04dba5f208fd5cb810078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084189"
---
# <a name="ienummediaskip-method"></a><span data-ttu-id="c4177-103">Metodo IEnumMedia::Skip</span><span class="sxs-lookup"><span data-stu-id="c4177-103">IEnumMedia::Skip method</span></span>

<span data-ttu-id="c4177-104">\[ I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c4177-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c4177-105">L'API client RTC offre funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="c4177-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c4177-106">Il **metodo Skip** ignora il successivo numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="c4177-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4177-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4177-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="c4177-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4177-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4177-109">*celt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4177-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4177-110">Numero di elementi da ignorare.</span><span class="sxs-lookup"><span data-stu-id="c4177-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4177-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4177-111">Return value</span></span>

<span data-ttu-id="c4177-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c4177-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c4177-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c4177-113">Return code</span></span>                                                                             | <span data-ttu-id="c4177-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4177-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="c4177-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4177-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c4177-116">Numero di elementi *ignorati.*</span><span class="sxs-lookup"><span data-stu-id="c4177-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="c4177-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c4177-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c4177-118">Il numero di elementi ignorati non è *stato cel*.</span><span class="sxs-lookup"><span data-stu-id="c4177-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c4177-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4177-119">Requirements</span></span>



| <span data-ttu-id="c4177-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4177-120">Requirement</span></span> | <span data-ttu-id="c4177-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c4177-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4177-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="c4177-122">TAPI version</span></span><br/> | <span data-ttu-id="c4177-123">Richiede TAPI 3.0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c4177-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c4177-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4177-124">Header</span></span><br/>       | <dl> <span data-ttu-id="c4177-125"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="c4177-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4177-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4177-126">Library</span></span><br/>      | <dl> <span data-ttu-id="c4177-127"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4177-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c4177-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c4177-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="c4177-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4177-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4177-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4177-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4177-131">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="c4177-131">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




