---
description: Il metodo Configure Invia le informazioni di configurazione per un'acquisizione.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'Metodo IESP:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305880"
---
# <a name="iespconfigure-method"></a><span data-ttu-id="05872-103">Metodo IESP:: Configure</span><span class="sxs-lookup"><span data-stu-id="05872-103">IESP::Configure method</span></span>

<span data-ttu-id="05872-104">Il metodo **Configure** Invia le informazioni di configurazione per un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="05872-104">The **Configure** method submits configuration information for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="05872-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05872-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="05872-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="05872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05872-107">*hConfigurationBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05872-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05872-108">Handle per il BLOB configurato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="05872-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="05872-109">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="05872-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05872-110">Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="05872-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="05872-111">Per informazioni sul contenuto di un BLOB di errore, vedere la sezione Osservazioni in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="05872-111">For information about the contents of an error BLOB, see the Remarks section in this topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05872-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05872-112">Return value</span></span>

<span data-ttu-id="05872-113">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="05872-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="05872-114">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="05872-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="05872-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="05872-115">Return code</span></span>                                                                                                         | <span data-ttu-id="05872-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05872-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05872-117"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-117"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>                | <span data-ttu-id="05872-118">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="05872-118">The NPP is not connected to the network.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="05872-119"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>                      | <span data-ttu-id="05872-120">L'oggetto NPP è connesso alla rete, ma non con il metodo [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="05872-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="05872-121"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-121"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                     | <span data-ttu-id="05872-122">Il NPP segnala che la sessione di acquisizione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="05872-122">The NPP reports that the capture session has started.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="05872-123"><dt>**TRIGGER NMERR non \_ valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-123"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="05872-124">La parte del trigger del BLOB di configurazione è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="05872-124">The trigger portion of the configuration BLOB is corrupt.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="05872-125"><dt>**\_la voce del BLOB NMERR non \_ \_ \_ \_ esiste**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-125"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="05872-126">Per il BLOB di configurazione specificato da *hConfigurationBlob* manca una voce necessaria per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="05872-126">The configuration BLOB specified by *hConfigurationBlob* is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="05872-127">Esaminare il BLOB di errore restituito da *hErrorBlob* per determinare quale voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="05872-127">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="05872-128"><dt>**\_errore di \_ conversione \_ BLOB NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-128"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="05872-129">Il BLOB è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="05872-129">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="05872-130"><dt>**\_BLOB NMERR \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-130"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="05872-131">Il metodo **CreateBlob** non è stato chiamato.</span><span class="sxs-lookup"><span data-stu-id="05872-131">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="05872-132"><dt>**\_BLOB NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-132"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="05872-133">L'oggetto a cui si fa riferimento non è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="05872-133">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="05872-134"><dt>**\_stringa BLOB \_ NMERR \_ non valida**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-134"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="05872-135">La stringa non termina con null.</span><span class="sxs-lookup"><span data-stu-id="05872-135">The string is not null-terminated.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="05872-136"><dt>**BLOB a livello di NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-136"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="05872-137">Il numero di versione del BLOB non è corretto.</span><span class="sxs-lookup"><span data-stu-id="05872-137">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="05872-138"><dt>**\_ \_ \_ memoria insufficiente NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-138"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="05872-139">Memoria non disponibile.</span><span class="sxs-lookup"><span data-stu-id="05872-139">No memory was available.</span></span> <span data-ttu-id="05872-140">Arrestare Windows per liberare risorse.</span><span class="sxs-lookup"><span data-stu-id="05872-140">Shut down windows to free up resources.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="05872-141"><dt>**\_timeout NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="05872-141"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="05872-142">Timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="05872-142">The request has timed out.</span></span><br/>                                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="05872-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="05872-143">Remarks</span></span>

<span data-ttu-id="05872-144">È necessario applicare questo metodo per riavviare un oggetto NPP che è stato avviato e arrestato, ma non disconnesso.</span><span class="sxs-lookup"><span data-stu-id="05872-144">You must apply this method to restart an NPP that has been started and stopped, but not disconnected.</span></span>

<span data-ttu-id="05872-145">Il BLOB di errori restituito dal parametro *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di configurazione specificato in *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="05872-145">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="05872-146">Il BLOB di errori restituito contiene informazioni sugli errori che possono essere utilizzate dall'applicazione per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="05872-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="05872-147">Ad esempio, se \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="05872-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="05872-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05872-148">Requirements</span></span>



| <span data-ttu-id="05872-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="05872-149">Requirement</span></span> | <span data-ttu-id="05872-150">Valore</span><span class="sxs-lookup"><span data-stu-id="05872-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05872-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05872-151">Minimum supported client</span></span><br/> | <span data-ttu-id="05872-152">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="05872-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="05872-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05872-153">Minimum supported server</span></span><br/> | <span data-ttu-id="05872-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="05872-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="05872-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05872-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="05872-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="05872-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="05872-157">DLL</span><span class="sxs-lookup"><span data-stu-id="05872-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05872-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05872-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

 




