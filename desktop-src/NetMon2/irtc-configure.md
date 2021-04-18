---
description: Invia i dati di configurazione per un'acquisizione dei dati.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'Metodo IRTC:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306558"
---
# <a name="irtcconfigure-method"></a><span data-ttu-id="03473-103">Metodo IRTC:: Configure</span><span class="sxs-lookup"><span data-stu-id="03473-103">IRTC::Configure method</span></span>

<span data-ttu-id="03473-104">Il metodo [**Configure**](configure.md) invia i dati di configurazione per un'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="03473-104">The [**Configure**](configure.md) method submits configuration data for a data capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="03473-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03473-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="03473-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03473-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03473-107">*hConfigurationBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03473-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03473-108">Handle per il BLOB configurato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="03473-108">A handle to the BLOB that is configured by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="03473-109">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="03473-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03473-110">Handle per un BLOB di errori che contiene dati di errore aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="03473-110">A handle to an error BLOB that contains additional error data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03473-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03473-111">Return value</span></span>

<span data-ttu-id="03473-112">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="03473-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="03473-113">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="03473-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="03473-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="03473-114">Return code</span></span>                                                                                                         | <span data-ttu-id="03473-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03473-115">Description</span></span>                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03473-116"><dt>**\_BLOB NMERR \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-116"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="03473-117">Il metodo **CreateBlob** non è stato chiamato.</span><span class="sxs-lookup"><span data-stu-id="03473-117">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                 |
| <dl> <span data-ttu-id="03473-118"><dt>**\_BLOB NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-118"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="03473-119">L'oggetto a cui fa riferimento non è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="03473-119">The object pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="03473-120"><dt>**BLOB a livello di NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-120"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="03473-121">Il numero di versione del BLOB non è corretto.</span><span class="sxs-lookup"><span data-stu-id="03473-121">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="03473-122"><dt>**la \_ voce del BLOB NMERR \_ \_ \_ esiste già**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-122"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="03473-123">BLOB duplicato.</span><span class="sxs-lookup"><span data-stu-id="03473-123">Duplicate BLOB.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="03473-124"><dt>**\_la voce del BLOB NMERR non \_ \_ \_ \_ esiste**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-124"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="03473-125">Il BLOB di configurazione specificato da *hConfigurationBlob* non dispone di una voce necessaria per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="03473-125">The configuration BLOB specified by *hConfigurationBlob* lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="03473-126">Visualizzare il BLOB di errore restituito da *hErrorBlob* per determinare quale voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="03473-126">View the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="03473-127"><dt>**\_identificatore ambiguo NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-127"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="03473-128">Mancano i dati del proprietario o della categoria del BLOB.</span><span class="sxs-lookup"><span data-stu-id="03473-128">The BLOB Owner or Category data is missing.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="03473-129"><dt>**il \_ proprietario del BLOB NMERR non è stato \_ \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-129"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="03473-130">La sezione del proprietario del BLOB non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="03473-130">The BLOB Owner section was not found.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="03473-131"><dt>**\_categoria BLOB \_ NMERR \_ non \_ trovata**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-131"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="03473-132">La sezione della categoria BLOB non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="03473-132">The BLOB Category section was not found.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="03473-133"><dt>**\_categoria NMERR sconosciuta \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-133"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="03473-134">La sezione relativa alla categoria BLOB è stata trovata, ma non è stata riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="03473-134">The BLOB Category section was found, but not understood.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="03473-135"><dt>**NMERR \_ \_ tag sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-135"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="03473-136">La sezione del tag BLOB è stata trovata, ma non è stata riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="03473-136">The BLOB Tag section was found, but not understood.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="03473-137"><dt>**\_errore di \_ conversione \_ BLOB NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-137"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="03473-138">Il BLOB è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="03473-138">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="03473-139"><dt>**TRIGGER NMERR non \_ valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-139"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="03473-140">La parte del trigger del BLOB è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="03473-140">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="03473-141"><dt>**\_stringa BLOB \_ NMERR \_ non valida**</dt></span><span class="sxs-lookup"><span data-stu-id="03473-141"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="03473-142">La stringa non termina con null.</span><span class="sxs-lookup"><span data-stu-id="03473-142">The string is not null-terminated.</span></span><br/>                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="03473-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="03473-143">Remarks</span></span>

<span data-ttu-id="03473-144">È necessario applicare questo metodo per riavviare un oggetto NPP che è stato avviato, arrestato, ma non disconnesso.</span><span class="sxs-lookup"><span data-stu-id="03473-144">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="03473-145">Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di configurazione specificato in *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="03473-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="03473-146">Il BLOB di errori restituito contiene i dati di errore che possono essere usati dall'applicazione per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="03473-146">The returned error BLOB contains error data that the application can use for troubleshooting.</span></span> <span data-ttu-id="03473-147">Se, ad esempio, \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="03473-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor cannot find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="03473-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03473-148">Requirements</span></span>



| <span data-ttu-id="03473-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="03473-149">Requirement</span></span> | <span data-ttu-id="03473-150">Valore</span><span class="sxs-lookup"><span data-stu-id="03473-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03473-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03473-151">Minimum supported client</span></span><br/> | <span data-ttu-id="03473-152">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03473-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="03473-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03473-153">Minimum supported server</span></span><br/> | <span data-ttu-id="03473-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03473-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="03473-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03473-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="03473-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="03473-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="03473-157">DLL</span><span class="sxs-lookup"><span data-stu-id="03473-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03473-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03473-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03473-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03473-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03473-160">IRTC</span><span class="sxs-lookup"><span data-stu-id="03473-160">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="03473-161">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="03473-161">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="03473-162">BLOB Network Monitor</span><span class="sxs-lookup"><span data-stu-id="03473-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




