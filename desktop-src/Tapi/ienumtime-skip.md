---
description: Il metodo Skip ignora il successivo numero specificato di elementi nella sequenza di enumerazione.
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: 'Metodo IEnumTime:: Skip (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebd157afc51f52a8453c38f8a14702476c46eb9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330746"
---
# <a name="ienumtimeskip-method"></a><span data-ttu-id="e8e1c-103">Metodo IEnumTime:: Skip</span><span class="sxs-lookup"><span data-stu-id="e8e1c-103">IEnumTime::Skip method</span></span>

<span data-ttu-id="e8e1c-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e8e1c-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e8e1c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e8e1c-106">Il metodo **Skip** ignora il successivo numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e1c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8e1c-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="e8e1c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8e1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e1c-109">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8e1c-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8e1c-110">Numero di elementi da ignorare.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e1c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8e1c-111">Return value</span></span>

<span data-ttu-id="e8e1c-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e8e1c-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e8e1c-113">Return code</span></span>                                                                             | <span data-ttu-id="e8e1c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8e1c-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="e8e1c-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8e1c-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e8e1c-116">Il numero di elementi ignorati è *celt*.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="e8e1c-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e8e1c-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e8e1c-118">Il numero di elementi ignorati non è *celt*.</span><span class="sxs-lookup"><span data-stu-id="e8e1c-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8e1c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8e1c-119">Requirements</span></span>



| <span data-ttu-id="e8e1c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e1c-120">Requirement</span></span> | <span data-ttu-id="e8e1c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e8e1c-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e1c-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e8e1c-122">TAPI version</span></span><br/> | <span data-ttu-id="e8e1c-123">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e8e1c-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e8e1c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8e1c-124">Header</span></span><br/>       | <dl> <span data-ttu-id="e8e1c-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e1c-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8e1c-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8e1c-126">Library</span></span><br/>      | <dl> <span data-ttu-id="e8e1c-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8e1c-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e8e1c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e8e1c-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="e8e1c-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8e1c-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e1c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8e1c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e1c-131">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="e8e1c-131">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




