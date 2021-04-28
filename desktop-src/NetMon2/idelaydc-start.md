---
description: "Metodo IDelaydC::Start: il metodo Start avvia un'acquisizione."
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: Metodo IDelaydC::Start (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25bf778d9cccce20c736c5f8b83e6af9754ac933
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118439"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="34490-103">Metodo IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="34490-103">IDelaydC::Start method</span></span>

<span data-ttu-id="34490-104">Il **metodo Start** avvia un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="34490-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="34490-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34490-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="34490-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34490-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34490-107">*pFileName* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="34490-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34490-108">Puntatore al nome del [*file di acquisizione utilizzato*](c.md) per archiviare i dati di rete.</span><span class="sxs-lookup"><span data-stu-id="34490-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="34490-109">Assicurarsi di memorizzare nella cache questo nome file se necessario per riferimento futuro.</span><span class="sxs-lookup"><span data-stu-id="34490-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34490-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34490-110">Return value</span></span>

<span data-ttu-id="34490-111">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="34490-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="34490-112">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="34490-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="34490-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="34490-113">Return code</span></span>                                                                                           | <span data-ttu-id="34490-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34490-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34490-115"><dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt></span><span class="sxs-lookup"><span data-stu-id="34490-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="34490-116">L'acquisizione è in stato di sospensione e deve essere arrestata prima di poter essere riavviata.</span><span class="sxs-lookup"><span data-stu-id="34490-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="34490-117">Chiamare [**IDelaydC::Stop per**](idelaydc-stop.md) arrestare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="34490-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="34490-118">Per altre informazioni, vedere la sezione Osservazioni in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="34490-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="34490-119"><dt>**ACQUISIZIONE DI \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="34490-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="34490-120">L'acquisizione è già stata avviata.</span><span class="sxs-lookup"><span data-stu-id="34490-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="34490-121"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="34490-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="34490-122">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="34490-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="34490-123">Chiamare [**IDelaydC::Connect**](idelaydc-connect.md) per connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="34490-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="34490-124"><dt>**NMERR \_ NON \_ RITARDATO**</dt></span><span class="sxs-lookup"><span data-stu-id="34490-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="34490-125">Il NPP è connesso alla rete, ma non con il [**metodo IDelaydC::Connect.**](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="34490-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="34490-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="34490-126">Remarks</span></span>

<span data-ttu-id="34490-127">Il percorso del [*file di acquisizione*](c.md) è specificato nel Registro di sistema di Windows, ma è possibile usare Network Monitor per modificare il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="34490-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="34490-128">Per riavviare l'acquisizione usando **IDelaydC::Start** e [**IDelaydC::Stop,**](idelaydc-stop.md)è necessario chiamare il metodo [**IDelaydC::Configure**](idelaydc-configure.md) per riconfigurare la connessione ogni volta che si chiama il metodo **IDelaydC::Start** per riavviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="34490-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="34490-129">Quando si avvia e si arresta l'acquisizione con questi tre metodi, viene creato un nuovo file di acquisizione a ogni avvio dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="34490-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="34490-130">È anche possibile avviare e arrestare l'acquisizione usando i metodi [**IDelaydC::P ause**](idelaydc-pause.md) e [**IDelaydC::Resume.**](idelaydc-resume.md)</span><span class="sxs-lookup"><span data-stu-id="34490-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="34490-131">Quando si usano questi due metodi, i dati acquisiti vengono archiviati nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="34490-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34490-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34490-132">Requirements</span></span>



| <span data-ttu-id="34490-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="34490-133">Requirement</span></span> | <span data-ttu-id="34490-134">Valore</span><span class="sxs-lookup"><span data-stu-id="34490-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34490-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34490-135">Minimum supported client</span></span><br/> | <span data-ttu-id="34490-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="34490-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="34490-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34490-137">Minimum supported server</span></span><br/> | <span data-ttu-id="34490-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="34490-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="34490-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34490-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="34490-140"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="34490-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="34490-141">DLL</span><span class="sxs-lookup"><span data-stu-id="34490-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34490-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34490-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34490-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34490-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34490-144">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="34490-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="34490-145">**IDelaydC::Configure**</span><span class="sxs-lookup"><span data-stu-id="34490-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="34490-146">**IDelaydC::Connect**</span><span class="sxs-lookup"><span data-stu-id="34490-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="34490-147">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="34490-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="34490-148">**IDelaydC::Resume**</span><span class="sxs-lookup"><span data-stu-id="34490-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="34490-149">**IDelaydC::Stop**</span><span class="sxs-lookup"><span data-stu-id="34490-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




