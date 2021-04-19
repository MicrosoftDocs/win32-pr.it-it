---
description: Il metodo SetPortInfo imposta il valore della porta a 16 bit per la prima porta e il numero di porte necessarie per una sessione.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'Metodo ITMedia:: SetPortInfo (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332923"
---
# <a name="itmediasetportinfo-method"></a><span data-ttu-id="0db89-103">Metodo ITMedia:: SetPortInfo</span><span class="sxs-lookup"><span data-stu-id="0db89-103">ITMedia::SetPortInfo method</span></span>

<span data-ttu-id="0db89-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0db89-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0db89-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0db89-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0db89-106">Il metodo **SetPortInfo** imposta il valore della porta a 16 bit per la prima porta e il numero di porte necessarie per una sessione.</span><span class="sxs-lookup"><span data-stu-id="0db89-106">The **SetPortInfo** method sets the 16-bit port value for the first port and the number of ports needed for a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db89-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0db89-107">Syntax</span></span>


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="0db89-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0db89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db89-109">*Presenta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0db89-109">*StartPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db89-110">Porta iniziale.</span><span class="sxs-lookup"><span data-stu-id="0db89-110">Starting port.</span></span> <span data-ttu-id="0db89-111">Può trattarsi di un valore compreso nell'intervallo 0-65535.</span><span class="sxs-lookup"><span data-stu-id="0db89-111">This can be a value in the range 0-65535.</span></span>

</dd> <dt>

<span data-ttu-id="0db89-112">*NumPorts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0db89-112">*NumPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db89-113">Numero di porte.</span><span class="sxs-lookup"><span data-stu-id="0db89-113">Number of ports.</span></span> <span data-ttu-id="0db89-114">Può trattarsi di un valore compreso nell'intervallo 0-65535.</span><span class="sxs-lookup"><span data-stu-id="0db89-114">This can be a value in the range 0-65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db89-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0db89-115">Return value</span></span>

<span data-ttu-id="0db89-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0db89-116">This method can return one of these values.</span></span>



| <span data-ttu-id="0db89-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0db89-117">Return code</span></span>                                                                                   | <span data-ttu-id="0db89-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0db89-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0db89-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0db89-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0db89-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0db89-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0db89-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0db89-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0db89-122">Il parametro *presenta o NumPorts* non è valido.</span><span class="sxs-lookup"><span data-stu-id="0db89-122">The *StartPort or NumPorts* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="0db89-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0db89-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0db89-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0db89-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0db89-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="0db89-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0db89-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0db89-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0db89-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0db89-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0db89-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="0db89-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0db89-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="0db89-129">Remarks</span></span>

<span data-ttu-id="0db89-130">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="0db89-130">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="0db89-131">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0db89-131">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db89-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0db89-132">Requirements</span></span>



| <span data-ttu-id="0db89-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db89-133">Requirement</span></span> | <span data-ttu-id="0db89-134">Valore</span><span class="sxs-lookup"><span data-stu-id="0db89-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0db89-135">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0db89-135">TAPI version</span></span><br/> | <span data-ttu-id="0db89-136">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0db89-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0db89-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0db89-137">Header</span></span><br/>       | <dl> <span data-ttu-id="0db89-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db89-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0db89-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="0db89-139">Library</span></span><br/>      | <dl> <span data-ttu-id="0db89-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0db89-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0db89-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0db89-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="0db89-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db89-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db89-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0db89-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db89-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="0db89-144">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




