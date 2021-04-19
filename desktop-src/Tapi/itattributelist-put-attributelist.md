---
description: Il \_ metodo Put Attribute List imposta l'elenco di attributi.
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: 'ITAttributeList: metodo:p ut_AttributeList (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3876b2cd8ecdef46a933ff3f3c91be96dd028892
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332728"
---
# <a name="itattributelistput_attributelist-method"></a><span data-ttu-id="80e7e-103">ITAttributeList::p UT ( \_ Metodo Attribute)</span><span class="sxs-lookup"><span data-stu-id="80e7e-103">ITAttributeList::put\_AttributeList method</span></span>

<span data-ttu-id="80e7e-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="80e7e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="80e7e-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="80e7e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="80e7e-106">Il metodo **put \_ attribute** list imposta l'elenco di attributi.</span><span class="sxs-lookup"><span data-stu-id="80e7e-106">The **put\_AttributeList** method sets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e7e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80e7e-107">Syntax</span></span>


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="80e7e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="80e7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e7e-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80e7e-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e7e-110">Matrice di attributi da impostare.</span><span class="sxs-lookup"><span data-stu-id="80e7e-110">Array of attributes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e7e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80e7e-111">Return value</span></span>

<span data-ttu-id="80e7e-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="80e7e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="80e7e-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="80e7e-113">Return code</span></span>                                                                                   | <span data-ttu-id="80e7e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80e7e-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="80e7e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80e7e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="80e7e-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="80e7e-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="80e7e-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="80e7e-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="80e7e-118">Il parametro *newVal* non è valido.</span><span class="sxs-lookup"><span data-stu-id="80e7e-118">The *newVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="80e7e-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="80e7e-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="80e7e-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="80e7e-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="80e7e-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="80e7e-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="80e7e-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="80e7e-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="80e7e-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="80e7e-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="80e7e-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="80e7e-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="80e7e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80e7e-125">Requirements</span></span>



| <span data-ttu-id="80e7e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e7e-126">Requirement</span></span> | <span data-ttu-id="80e7e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="80e7e-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80e7e-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="80e7e-128">TAPI version</span></span><br/> | <span data-ttu-id="80e7e-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="80e7e-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="80e7e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80e7e-130">Header</span></span><br/>       | <dl> <span data-ttu-id="80e7e-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="80e7e-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="80e7e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="80e7e-132">Library</span></span><br/>      | <dl> <span data-ttu-id="80e7e-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80e7e-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="80e7e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="80e7e-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="80e7e-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80e7e-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e7e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80e7e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e7e-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="80e7e-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="80e7e-138">**ITAttributeList:: Get ( \_ attributo)**</span><span class="sxs-lookup"><span data-stu-id="80e7e-138">**ITAttributeList::get\_AttributeList**</span></span>](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




