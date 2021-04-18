---
description: Il metodo Start avvia un'acquisizione.
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'Metodo IDelaydC:: Start (Netmon. h)'
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
ms.openlocfilehash: a912af44dddb8a25d3279a5cdd7f021646c26e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305882"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="adfa7-103">Metodo IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="adfa7-103">IDelaydC::Start method</span></span>

<span data-ttu-id="adfa7-104">Il metodo **Start** avvia un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="adfa7-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="adfa7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="adfa7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="adfa7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="adfa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adfa7-107">*pFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="adfa7-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adfa7-108">Puntatore al nome del file di [*acquisizione*](c.md) usato per archiviare i dati di rete.</span><span class="sxs-lookup"><span data-stu-id="adfa7-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="adfa7-109">Assicurarsi di memorizzare nella cache il nome del file, se necessario, per riferimento futuro.</span><span class="sxs-lookup"><span data-stu-id="adfa7-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adfa7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="adfa7-110">Return value</span></span>

<span data-ttu-id="adfa7-111">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="adfa7-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="adfa7-112">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="adfa7-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="adfa7-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="adfa7-113">Return code</span></span>                                                                                           | <span data-ttu-id="adfa7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adfa7-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="adfa7-115"><dt>**\_acquisizione NMERR \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="adfa7-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="adfa7-116">L'acquisizione si trova in uno stato di sospensione e deve essere arrestata prima di poter essere riavviata.</span><span class="sxs-lookup"><span data-stu-id="adfa7-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="adfa7-117">Chiamare [**IDelaydC:: Stop**](idelaydc-stop.md) per arrestare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="adfa7-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="adfa7-118">Per ulteriori informazioni, vedere la sezione Osservazioni in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="adfa7-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="adfa7-119"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="adfa7-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="adfa7-120">Acquisizione già avviata.</span><span class="sxs-lookup"><span data-stu-id="adfa7-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="adfa7-121"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="adfa7-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="adfa7-122">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="adfa7-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="adfa7-123">Chiamare [**IDelaydC:: Connect**](idelaydc-connect.md) per connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="adfa7-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="adfa7-124"><dt>**NMERR \_ non \_ ritardato**</dt></span><span class="sxs-lookup"><span data-stu-id="adfa7-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="adfa7-125">L'oggetto NPP è connesso alla rete, ma non con il metodo [**IDelaydC:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="adfa7-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="adfa7-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="adfa7-126">Remarks</span></span>

<span data-ttu-id="adfa7-127">Il percorso del [*file di acquisizione*](c.md) è specificato nel registro di sistema di Windows, ma è possibile usare Network Monitor per modificare il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="adfa7-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="adfa7-128">Per riavviare l'acquisizione usando **IDelaydC:: Start** e [**IDelaydC:: Stop**](idelaydc-stop.md), è necessario chiamare il metodo [**IDelaydC:: Configure**](idelaydc-configure.md) per riconfigurare la connessione ogni volta che si chiama il metodo **IDelaydC:: Start** per riavviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="adfa7-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="adfa7-129">Quando si avvia e si arresta l'acquisizione con questi tre metodi, viene creato un nuovo file di acquisizione ogni volta che viene avviata l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="adfa7-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="adfa7-130">È anche possibile avviare e arrestare l'acquisizione usando i metodi [**IDelaydC::P ause**](idelaydc-pause.md) e [**IDelaydC:: Resume**](idelaydc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="adfa7-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="adfa7-131">Quando si usano questi due metodi, i dati acquisiti vengono archiviati nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="adfa7-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="adfa7-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="adfa7-132">Requirements</span></span>



| <span data-ttu-id="adfa7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="adfa7-133">Requirement</span></span> | <span data-ttu-id="adfa7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="adfa7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adfa7-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adfa7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="adfa7-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="adfa7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="adfa7-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adfa7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="adfa7-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="adfa7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="adfa7-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="adfa7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="adfa7-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="adfa7-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="adfa7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="adfa7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adfa7-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adfa7-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adfa7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="adfa7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adfa7-144">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="adfa7-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="adfa7-145">**IDelaydC:: Configure**</span><span class="sxs-lookup"><span data-stu-id="adfa7-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="adfa7-146">**IDelaydC:: Connect**</span><span class="sxs-lookup"><span data-stu-id="adfa7-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="adfa7-147">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="adfa7-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="adfa7-148">**IDelaydC:: Resume**</span><span class="sxs-lookup"><span data-stu-id="adfa7-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="adfa7-149">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="adfa7-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




