---
description: Il metodo SetPhoneNumbers imposta una matrice di numeri di telefono associati a un BLOB di conferenze.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'Metodo ITSdp:: SetPhoneNumbers (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329325"
---
# <a name="itsdpsetphonenumbers-method"></a><span data-ttu-id="a841f-103">Metodo ITSdp:: SetPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="a841f-103">ITSdp::SetPhoneNumbers method</span></span>

<span data-ttu-id="a841f-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a841f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a841f-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a841f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a841f-106">Il metodo **SetPhoneNumbers** imposta una matrice di numeri di telefono associati a un BLOB di conferenze.</span><span class="sxs-lookup"><span data-stu-id="a841f-106">The **SetPhoneNumbers** method sets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="a841f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a841f-107">Syntax</span></span>


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="a841f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a841f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a841f-109">*Numeri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a841f-109">*Numbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a841f-110">SAFEARRAY di **BSTR** s che elenca i numeri di telefono.</span><span class="sxs-lookup"><span data-stu-id="a841f-110">SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="a841f-111">*Nomi* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a841f-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a841f-112">SAFEARRAY dei nomi degli elenchi di **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="a841f-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a841f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a841f-113">Return value</span></span>

<span data-ttu-id="a841f-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a841f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a841f-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a841f-115">Return code</span></span>                                                                                   | <span data-ttu-id="a841f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a841f-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a841f-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a841f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a841f-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a841f-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a841f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a841f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a841f-120">Il parametro *numeri* o *nomi* non è valido.</span><span class="sxs-lookup"><span data-stu-id="a841f-120">The *Numbers* or *Names* parameter is not valid.</span></span><br/>     |
| <dl> <span data-ttu-id="a841f-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a841f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a841f-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a841f-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a841f-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="a841f-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a841f-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a841f-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a841f-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a841f-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a841f-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="a841f-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a841f-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a841f-127">Remarks</span></span>

<span data-ttu-id="a841f-128">Gli elenchi a cui puntano i *numeri* e i *nomi* sono della stessa lunghezza.</span><span class="sxs-lookup"><span data-stu-id="a841f-128">The lists that *Numbers* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="a841f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a841f-129">Requirements</span></span>



| <span data-ttu-id="a841f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a841f-130">Requirement</span></span> | <span data-ttu-id="a841f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a841f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a841f-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a841f-132">TAPI version</span></span><br/> | <span data-ttu-id="a841f-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a841f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a841f-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a841f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="a841f-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a841f-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a841f-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="a841f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="a841f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a841f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a841f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a841f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="a841f-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a841f-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a841f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a841f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a841f-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="a841f-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




