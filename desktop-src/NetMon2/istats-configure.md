---
description: Il metodo Configure Invia le informazioni di configurazione di acquisizione.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'Metodo IStats:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233303"
---
# <a name="istatsconfigure-method"></a><span data-ttu-id="edf1c-103">IStats:: Configure (metodo)</span><span class="sxs-lookup"><span data-stu-id="edf1c-103">IStats::Configure method</span></span>

<span data-ttu-id="edf1c-104">Il metodo **Configure** Invia le informazioni di configurazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="edf1c-104">The **Configure** method submits capture configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="edf1c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edf1c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="edf1c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="edf1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edf1c-107">*hConfigurationBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edf1c-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf1c-108">Handle per il BLOB configurato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="edf1c-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="edf1c-109">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edf1c-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edf1c-110">Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="edf1c-110">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edf1c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edf1c-111">Return value</span></span>

<span data-ttu-id="edf1c-112">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="edf1c-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="edf1c-113">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="edf1c-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="edf1c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="edf1c-114">Return code</span></span>                                                                                                         | <span data-ttu-id="edf1c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edf1c-115">Description</span></span>                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="edf1c-116"><dt>**\_stringa BLOB \_ NMERR \_ non valida**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-116"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="edf1c-117">La stringa non termina con null.</span><span class="sxs-lookup"><span data-stu-id="edf1c-117">The string is not null-terminated.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="edf1c-118"><dt>**\_BLOB NMERR \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-118"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="edf1c-119">Il metodo **CreateBlob** non è stato chiamato.</span><span class="sxs-lookup"><span data-stu-id="edf1c-119">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="edf1c-120"><dt>**\_BLOB NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-120"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="edf1c-121">L'oggetto a cui si fa riferimento non è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="edf1c-121">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="edf1c-122"><dt>**BLOB a livello di NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-122"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="edf1c-123">Il numero di versione del BLOB non è corretto.</span><span class="sxs-lookup"><span data-stu-id="edf1c-123">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="edf1c-124"><dt>**la \_ voce del BLOB NMERR \_ \_ \_ esiste già**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-124"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="edf1c-125">Una voce di BLOB esiste già.</span><span class="sxs-lookup"><span data-stu-id="edf1c-125">A BLOB entry already exists.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="edf1c-126"><dt>**\_la voce del BLOB NMERR non \_ \_ \_ \_ esiste**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-126"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="edf1c-127">Il BLOB di configurazione specificato dal parametro *hConfigurationBlob* non dispone di una voce necessaria per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="edf1c-127">The configuration BLOB specified by the *hConfigurationBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="edf1c-128">Esaminare il BLOB di errori restituito dal parametro *hErrorBlob* per determinare quale voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="edf1c-128">Look at the error BLOB returned by the *hErrorBlob* parameter to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="edf1c-129"><dt>**\_identificatore ambiguo NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-129"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="edf1c-130">Il BLOB non dispone di informazioni sul proprietario o sulla categoria.</span><span class="sxs-lookup"><span data-stu-id="edf1c-130">The BLOB lacks owner or category information.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="edf1c-131"><dt>**il \_ proprietario del BLOB NMERR non è stato \_ \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-131"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="edf1c-132">La sezione Owner del BLOB non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="edf1c-132">The Owner section of the BLOB was not found.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="edf1c-133"><dt>**\_categoria BLOB \_ NMERR \_ non \_ trovata**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-133"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="edf1c-134">La sezione Category del BLOB non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="edf1c-134">The Category section of the BLOB was not found.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="edf1c-135"><dt>**\_categoria NMERR sconosciuta \_**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-135"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="edf1c-136">Le informazioni sulla categoria sono state trovate ma non comprese.</span><span class="sxs-lookup"><span data-stu-id="edf1c-136">Category information was found but not understood.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="edf1c-137"><dt>**NMERR \_ \_ tag sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-137"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="edf1c-138">Le informazioni sui tag sono state trovate ma non comprese.</span><span class="sxs-lookup"><span data-stu-id="edf1c-138">Tag information was found but not understood.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="edf1c-139"><dt>**\_errore di \_ conversione \_ BLOB NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-139"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="edf1c-140">Il BLOB è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="edf1c-140">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="edf1c-141"><dt>**TRIGGER NMERR non \_ valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-141"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="edf1c-142">La parte del trigger del BLOB è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="edf1c-142">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="edf1c-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="edf1c-143">Remarks</span></span>

<span data-ttu-id="edf1c-144">È necessario applicare questo metodo per riavviare un oggetto NPP che è stato avviato, arrestato ma non disconnesso.</span><span class="sxs-lookup"><span data-stu-id="edf1c-144">You must apply this method to restart an NPP that has been started, stopped but not disconnected.</span></span>

<span data-ttu-id="edf1c-145">Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di configurazione specificato nel parametro *hConfigurationBlob* .</span><span class="sxs-lookup"><span data-stu-id="edf1c-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in the *hConfigurationBlob* parameter.</span></span> <span data-ttu-id="edf1c-146">Il BLOB di errori restituito contiene informazioni sugli errori che possono essere utilizzate dall'applicazione per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="edf1c-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="edf1c-147">Ad esempio, se \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="edf1c-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="edf1c-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edf1c-148">Requirements</span></span>



| <span data-ttu-id="edf1c-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="edf1c-149">Requirement</span></span> | <span data-ttu-id="edf1c-150">Valore</span><span class="sxs-lookup"><span data-stu-id="edf1c-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edf1c-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edf1c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="edf1c-152">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="edf1c-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="edf1c-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edf1c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="edf1c-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="edf1c-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="edf1c-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edf1c-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="edf1c-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="edf1c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="edf1c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edf1c-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edf1c-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edf1c-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edf1c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf1c-160">IStats</span><span class="sxs-lookup"><span data-stu-id="edf1c-160">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="edf1c-161">ISTATs:: Connect</span><span class="sxs-lookup"><span data-stu-id="edf1c-161">ISTATS::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="edf1c-162">BLOB Network Monitor</span><span class="sxs-lookup"><span data-stu-id="edf1c-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




