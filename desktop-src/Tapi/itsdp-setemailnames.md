---
description: Il metodo SetEmailNames imposta una matrice di indirizzi di posta elettronica associati al BLOB della conferenza.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: 'Metodo ITSdp:: SetEmailNames (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ff31e66f5f69fe7fad43da5ec436c3f567cd49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329326"
---
# <a name="itsdpsetemailnames-method"></a><span data-ttu-id="2d532-103">Metodo ITSdp:: SetEmailNames</span><span class="sxs-lookup"><span data-stu-id="2d532-103">ITSdp::SetEmailNames method</span></span>

<span data-ttu-id="2d532-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2d532-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2d532-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2d532-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2d532-106">Il metodo **SetEmailNames** imposta una matrice di indirizzi di posta elettronica associati al BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="2d532-106">The **SetEmailNames** method sets an array of e-mail addresses associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d532-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d532-107">Syntax</span></span>


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="2d532-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d532-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d532-109">*Indirizzi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d532-109">*Addresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d532-110">SAFEARRAY di **BSTR** s che elenca gli indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="2d532-110">SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="2d532-111">*Nomi* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2d532-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d532-112">SAFEARRAY dei nomi degli elenchi di **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="2d532-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d532-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d532-113">Return value</span></span>

<span data-ttu-id="2d532-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2d532-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2d532-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2d532-115">Return code</span></span>                                                                                   | <span data-ttu-id="2d532-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d532-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2d532-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2d532-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2d532-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2d532-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2d532-120">Il parametro degli *indirizzi* o *dei nomi* non è valido.</span><span class="sxs-lookup"><span data-stu-id="2d532-120">The *Addresses* or *Names* parameter is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="2d532-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2d532-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2d532-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2d532-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2d532-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2d532-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2d532-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2d532-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="2d532-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2d532-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d532-127">Remarks</span></span>

<span data-ttu-id="2d532-128">Gli elenchi a cui puntano gli *indirizzi* e i *nomi* sono della stessa lunghezza.</span><span class="sxs-lookup"><span data-stu-id="2d532-128">The lists that *Addresses* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d532-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d532-129">Requirements</span></span>



| <span data-ttu-id="2d532-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d532-130">Requirement</span></span> | <span data-ttu-id="2d532-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2d532-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d532-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="2d532-132">TAPI version</span></span><br/> | <span data-ttu-id="2d532-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2d532-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2d532-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d532-134">Header</span></span><br/>       | <dl> <span data-ttu-id="2d532-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d532-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d532-136">Library</span></span><br/>      | <dl> <span data-ttu-id="2d532-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2d532-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2d532-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="2d532-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d532-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d532-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d532-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="2d532-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




