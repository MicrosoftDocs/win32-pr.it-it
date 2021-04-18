---
description: Il metodo Start avvia un'acquisizione.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'Metodo IESP:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310507"
---
# <a name="iespstart-method"></a><span data-ttu-id="11d85-103">Metodo IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="11d85-103">IESP::Start method</span></span>

<span data-ttu-id="11d85-104">Il metodo **Start** avvia un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="11d85-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="11d85-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11d85-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="11d85-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11d85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11d85-107">*pFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11d85-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11d85-108">Puntatore al nome del file di [*acquisizione*](c.md) usato per archiviare i dati di rete.</span><span class="sxs-lookup"><span data-stu-id="11d85-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="11d85-109">Assicurarsi di memorizzare nella cache il nome del file, se necessario, per riferimento futuro.</span><span class="sxs-lookup"><span data-stu-id="11d85-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11d85-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11d85-110">Return value</span></span>

<span data-ttu-id="11d85-111">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="11d85-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="11d85-112">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="11d85-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="11d85-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="11d85-113">Return code</span></span>                                                                                           | <span data-ttu-id="11d85-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11d85-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11d85-115"><dt>**\_acquisizione NMERR \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="11d85-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="11d85-116">L'acquisizione viene sospesa e deve essere arrestata prima di poter essere riavviata.</span><span class="sxs-lookup"><span data-stu-id="11d85-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="11d85-117">Chiamare [IESP:: Stop](iesp-stop.md) per arrestare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="11d85-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="11d85-118"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="11d85-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="11d85-119">Acquisizione già avviata.</span><span class="sxs-lookup"><span data-stu-id="11d85-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="11d85-120"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="11d85-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="11d85-121">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="11d85-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="11d85-122">Chiamare [IESP:: Connect](iesp-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="11d85-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="11d85-123"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="11d85-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="11d85-124">L'oggetto NPP è connesso alla rete, ma non con il metodo [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="11d85-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="11d85-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="11d85-125">Remarks</span></span>

<span data-ttu-id="11d85-126">Il percorso del [*file di acquisizione*](c.md) è specificato nel registro di sistema di Windows, ma è possibile usare Network Monitor per modificare il percorso della directory.</span><span class="sxs-lookup"><span data-stu-id="11d85-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="11d85-127">Quando si riavvia l'acquisizione usando i metodi IESP:: Start e [IESP:: Stop](iesp-stop.md) , è necessario chiamare il metodo [IESP:: Configure](iesp-configure.md) per riconfigurare la connessione ogni volta che si chiama IESP:: Start per riavviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="11d85-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="11d85-128">Quando si avvia e si arresta l'acquisizione con questi tre metodi, viene creato un nuovo file di acquisizione ogni volta che viene avviata l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="11d85-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="11d85-129">È anche possibile avviare e arrestare l'acquisizione usando i metodi [IESP::P ause](iesp-pause.md) e [IESP:: Resume](iesp-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="11d85-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="11d85-130">Quando si usano questi due metodi, i dati acquisiti vengono archiviati nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="11d85-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11d85-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11d85-131">Requirements</span></span>



| <span data-ttu-id="11d85-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d85-132">Requirement</span></span> | <span data-ttu-id="11d85-133">Valore</span><span class="sxs-lookup"><span data-stu-id="11d85-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11d85-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11d85-134">Minimum supported client</span></span><br/> | <span data-ttu-id="11d85-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11d85-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="11d85-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11d85-136">Minimum supported server</span></span><br/> | <span data-ttu-id="11d85-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11d85-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="11d85-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11d85-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="11d85-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d85-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="11d85-140">DLL</span><span class="sxs-lookup"><span data-stu-id="11d85-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11d85-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11d85-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d85-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11d85-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d85-143">IESP</span><span class="sxs-lookup"><span data-stu-id="11d85-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="11d85-144">IESP:: Configure</span><span class="sxs-lookup"><span data-stu-id="11d85-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="11d85-145">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="11d85-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="11d85-146">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="11d85-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="11d85-147">IESP:: Resume</span><span class="sxs-lookup"><span data-stu-id="11d85-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="11d85-148">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="11d85-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




