---
description: Il metodo Skip ignora il successivo numero specificato di elementi nella sequenza di enumerazione.
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'Metodo IEnumMedia:: Skip (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd950fd61ad6f6b2030b03d0d269854f86e3a02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333147"
---
# <a name="ienummediaskip-method"></a><span data-ttu-id="9eca4-103">Metodo IEnumMedia:: Skip</span><span class="sxs-lookup"><span data-stu-id="9eca4-103">IEnumMedia::Skip method</span></span>

<span data-ttu-id="9eca4-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9eca4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9eca4-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="9eca4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9eca4-106">Il metodo **Skip** ignora il successivo numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="9eca4-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eca4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eca4-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="9eca4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eca4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eca4-109">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9eca4-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eca4-110">Numero di elementi da ignorare.</span><span class="sxs-lookup"><span data-stu-id="9eca4-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eca4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eca4-111">Return value</span></span>

<span data-ttu-id="9eca4-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="9eca4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9eca4-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9eca4-113">Return code</span></span>                                                                             | <span data-ttu-id="9eca4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eca4-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="9eca4-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9eca4-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9eca4-116">Il numero di elementi ignorati è *celt*.</span><span class="sxs-lookup"><span data-stu-id="9eca4-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="9eca4-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9eca4-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9eca4-118">Il numero di elementi ignorati non è *celt*.</span><span class="sxs-lookup"><span data-stu-id="9eca4-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9eca4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eca4-119">Requirements</span></span>



| <span data-ttu-id="9eca4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eca4-120">Requirement</span></span> | <span data-ttu-id="9eca4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9eca4-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9eca4-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="9eca4-122">TAPI version</span></span><br/> | <span data-ttu-id="9eca4-123">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9eca4-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9eca4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9eca4-124">Header</span></span><br/>       | <dl> <span data-ttu-id="9eca4-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eca4-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9eca4-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="9eca4-126">Library</span></span><br/>      | <dl> <span data-ttu-id="9eca4-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eca4-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9eca4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9eca4-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="9eca4-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eca4-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eca4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eca4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eca4-131">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="9eca4-131">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




