---
description: Il metodo Configure Invia le informazioni di configurazione usate per un'acquisizione.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Metodo IDelaydCConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484316"
---
# <a name="idelaydcconfigure-method"></a><span data-ttu-id="130d1-103">Metodo IDelaydC:: Configure</span><span class="sxs-lookup"><span data-stu-id="130d1-103">IDelaydC::Configure method</span></span>

<span data-ttu-id="130d1-104">Il metodo **Configure** Invia le informazioni di configurazione usate per un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="130d1-104">The **Configure** method submits configuration information used for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="130d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="130d1-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="130d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="130d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="130d1-107">*hConfigurationBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="130d1-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="130d1-108">Handle per il BLOB che contiene le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="130d1-108">Handle to the BLOB that contains the configuration information.</span></span>

</dd> <dt>

<span data-ttu-id="130d1-109">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="130d1-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="130d1-110">Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="130d1-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="130d1-111">Per informazioni sul contenuto di un BLOB di errore, vedere la sezione Osservazioni in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="130d1-111">For information about the contents of an error BLOB, see the Remarks section in this topic .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="130d1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="130d1-112">Return value</span></span>

<span data-ttu-id="130d1-113">Se questo metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="130d1-113">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="130d1-114">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="130d1-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="130d1-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="130d1-115">Return code</span></span>                                                                                                      | <span data-ttu-id="130d1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="130d1-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="130d1-117"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="130d1-117"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                  | <span data-ttu-id="130d1-118">Il NPP segnala che la sessione di acquisizione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="130d1-118">The NPP reports that the capture session has started.</span></span><br/>                          |
| <dl> <span data-ttu-id="130d1-119"><dt>**\_disco NMERR \_ non \_ \_ fisso locale**</dt></span><span class="sxs-lookup"><span data-stu-id="130d1-119"><dt>**NMERR\_DISK\_NOT\_LOCAL\_FIXED**</dt></span></span> </dl>    |                                                                                           |
| <dl> <span data-ttu-id="130d1-120"><dt>**NMERR \_ non è in grado di \_ \_ creare \_ memoria**</dt></span><span class="sxs-lookup"><span data-stu-id="130d1-120"><dt>**NMERR\_COULD\_NOT\_CREATE\_MEMORY**</dt></span></span> </dl> |                                                                                           |
| <dl> <span data-ttu-id="130d1-121"><dt>**\_ \_ \_ memoria insufficiente NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="130d1-121"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>            | <span data-ttu-id="130d1-122">Memoria non disponibile.</span><span class="sxs-lookup"><span data-stu-id="130d1-122">No memory was available.</span></span> <span data-ttu-id="130d1-123">Arrestare Windows per liberare risorse.</span><span class="sxs-lookup"><span data-stu-id="130d1-123">Shut down windows to free up resources.</span></span><br/>               |
| <dl> <span data-ttu-id="130d1-124"><dt>**\_parametro NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="130d1-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="130d1-125">Il BLOB di configurazione specificato dal parametro hConfiguration non è valido.</span><span class="sxs-lookup"><span data-stu-id="130d1-125">The configuration BLOB specified by the hConfiguration parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="130d1-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="130d1-126">Remarks</span></span>

<span data-ttu-id="130d1-127">È necessario applicare questo metodo per riavviare un oggetto NPP che è stato avviato, arrestato, ma non disconnesso.</span><span class="sxs-lookup"><span data-stu-id="130d1-127">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="130d1-128">Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di configurazione specificato in *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="130d1-128">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="130d1-129">Il BLOB di errori restituito contiene informazioni sugli errori che possono essere utilizzate dall'applicazione per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="130d1-129">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="130d1-130">Ad esempio, se \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="130d1-130">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="130d1-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="130d1-131">Requirements</span></span>



| <span data-ttu-id="130d1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="130d1-132">Requirement</span></span> | <span data-ttu-id="130d1-133">Valore</span><span class="sxs-lookup"><span data-stu-id="130d1-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="130d1-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="130d1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="130d1-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="130d1-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="130d1-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="130d1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="130d1-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="130d1-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="130d1-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="130d1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="130d1-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="130d1-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="130d1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="130d1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="130d1-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="130d1-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="130d1-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="130d1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="130d1-143">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="130d1-143">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="130d1-144">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="130d1-144">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="130d1-145">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="130d1-145">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="130d1-146">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="130d1-146">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




