---
description: Il metodo Connect connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione relative alla connessione.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'Metodo IDelaydC:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2cd1fb5ad694493c4a225aa3bf109d7775b9dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878642"
---
# <a name="idelaydcconnect-method"></a><span data-ttu-id="95d0b-103">Metodo IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="95d0b-103">IDelaydC::Connect method</span></span>

<span data-ttu-id="95d0b-104">Il metodo **Connect** connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione relative alla connessione.</span><span class="sxs-lookup"><span data-stu-id="95d0b-104">The **Connect** method connects the NPP to the network by using a specified network interface card and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d0b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95d0b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="95d0b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="95d0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d0b-107">*hInputBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95d0b-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d0b-108">Handle per il BLOB che specifica la scheda di interfaccia di rete a cui ci si connette e le informazioni di configurazione relative a tale connessione.</span><span class="sxs-lookup"><span data-stu-id="95d0b-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information about that connection.</span></span>

</dd> <dt>

<span data-ttu-id="95d0b-109">*StatusCallbackProc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95d0b-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d0b-110">Indirizzo della funzione di callback dell'utente, che viene usata per ricevere gli aggiornamenti di stato, ad esempio i trigger.</span><span class="sxs-lookup"><span data-stu-id="95d0b-110">Address of the user's callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="95d0b-111">Se non viene usata alcuna funzione di callback, impostare questo parametro e il parametro *userContext* su **null**.</span><span class="sxs-lookup"><span data-stu-id="95d0b-111">If no callback function is used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95d0b-112">*UserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95d0b-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d0b-113">Valore passato quando viene chiamata la funzione di callback dell'utente.</span><span class="sxs-lookup"><span data-stu-id="95d0b-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="95d0b-114">Il valore di questo parametro è in genere HWND o un puntatore ' This '.</span><span class="sxs-lookup"><span data-stu-id="95d0b-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="95d0b-115">Se non viene specificata una funzione di callback, impostare questo parametro e il parametro *StatusCallbackProc* su **null**.</span><span class="sxs-lookup"><span data-stu-id="95d0b-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95d0b-116">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="95d0b-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95d0b-117">Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="95d0b-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d0b-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95d0b-118">Return value</span></span>

<span data-ttu-id="95d0b-119">Se questo metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="95d0b-119">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="95d0b-120">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti (che includono gli errori restituiti dalla chiamata interna **IDelaydC:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="95d0b-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IDelaydC::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95d0b-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="95d0b-121">Return code</span></span></th>
<th><span data-ttu-id="95d0b-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95d0b-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="95d0b-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-124">Questa istanza dell'oggetto COM NPP è già connessa alla rete.</span><span class="sxs-lookup"><span data-stu-id="95d0b-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="95d0b-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-126">Il BLOB di configurazione è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="95d0b-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="95d0b-127">Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-127">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="95d0b-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-129">Per il BLOB di input specificato da <em>hInputBlob</em> manca una voce necessaria per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="95d0b-129">The input BLOB specified by <em>hInputBlob</em> is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="95d0b-130">Questo errore può essere generato dalla chiamata <strong>IDelaydC:: Connect</strong> o <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-130">This error may be generated by the <strong>IDelaydC::Connect</strong> or <strong>IDelaydC::Configure</strong> call.</span></span> <span data-ttu-id="95d0b-131">Esaminare il BLOB di errore restituito da <em>hErrorBlob</em> per determinare quale voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="95d0b-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="95d0b-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-133">La funzione <strong>CreateBlob</strong> non è stata chiamata.</span><span class="sxs-lookup"><span data-stu-id="95d0b-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="95d0b-134">Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-134">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="95d0b-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-136">La stringa non termina con null.</span><span class="sxs-lookup"><span data-stu-id="95d0b-136">The string is not null-terminated.</span></span> <span data-ttu-id="95d0b-137">Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-137">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="95d0b-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-139">La parte del trigger del BLOB di input è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="95d0b-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="95d0b-140">Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-140">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="95d0b-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-142">L'oggetto specificato in <em>hInputBlob</em> non è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="95d0b-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="95d0b-143">Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-143">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="95d0b-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-145">La directory di acquisizione predefinita non è stata impostata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="95d0b-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="95d0b-146">Usare il percorso seguente per impostare la directory di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="95d0b-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="95d0b-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-148">Memoria non disponibile per l'esecuzione di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="95d0b-148">No memory was available to perform this operation.</span></span> <span data-ttu-id="95d0b-149">Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-149">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="95d0b-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-151">Timeout della richiesta. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-151">The request has timed out. This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="95d0b-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d0b-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="95d0b-153">Il numero di versione del BLOB specificato in <em>hInputBlob</em> non è corretto.</span><span class="sxs-lookup"><span data-stu-id="95d0b-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="95d0b-154">Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="95d0b-154">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="95d0b-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="95d0b-155">Remarks</span></span>

<span data-ttu-id="95d0b-156">Quando viene chiamato il metodo **Connect** , l'oggetto NPP chiama automaticamente **IDelaydC:: Configure** usando il BLOB fornito da *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="95d0b-156">When the **Connect** method is called, the NPP automatically calls **IDelaydC::Configure** by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="95d0b-157">Si noti che tutti i codici di errore restituiti dalla chiamata a **IDelaydC:: Configure** vengono passati nuovamente e restituiti dalla chiamata **IDelaydC:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="95d0b-157">Note that any error codes returned by the call to **IDelaydC::Configure** are passed back and returned by the **IDelaydC::Connect** call.</span></span>

<span data-ttu-id="95d0b-158">Questo metodo deve essere chiamato prima che sia possibile avviare l'acquisizione di frame.</span><span class="sxs-lookup"><span data-stu-id="95d0b-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="95d0b-159">Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare i metodi dell'interfaccia **IDelaydC** per acquisire i frame.</span><span class="sxs-lookup"><span data-stu-id="95d0b-159">Note that when you connect to the network by using this method, you must continue to use the **IDelaydC** interface methods to capture frames.</span></span>

<span data-ttu-id="95d0b-160">Il BLOB di input specificato dal parametro *hInputBlob* può essere ottenuto chiamando **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable**.</span><span class="sxs-lookup"><span data-stu-id="95d0b-160">The input BLOB specified by the *hInputBlob* parameter can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="95d0b-161">Il BLOB di errori restituito in *hErrorBlob* contiene informazioni sull'errore che lo sviluppatore o l'applicazione può utilizzare per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="95d0b-161">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="95d0b-162">Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di input specificato in *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="95d0b-162">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="95d0b-163">Ad esempio, se \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="95d0b-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="95d0b-164">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="95d0b-164">For information about</span></span>                          | <span data-ttu-id="95d0b-165">Vedere</span><span class="sxs-lookup"><span data-stu-id="95d0b-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="95d0b-166">Recupero del BLOB di input che rappresenta una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="95d0b-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="95d0b-167">Selezione di una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="95d0b-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="95d0b-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95d0b-168">Requirements</span></span>



| <span data-ttu-id="95d0b-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d0b-169">Requirement</span></span> | <span data-ttu-id="95d0b-170">Valore</span><span class="sxs-lookup"><span data-stu-id="95d0b-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d0b-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95d0b-171">Minimum supported client</span></span><br/> | <span data-ttu-id="95d0b-172">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="95d0b-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="95d0b-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95d0b-173">Minimum supported server</span></span><br/> | <span data-ttu-id="95d0b-174">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="95d0b-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="95d0b-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95d0b-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d0b-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d0b-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="95d0b-177">DLL</span><span class="sxs-lookup"><span data-stu-id="95d0b-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d0b-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d0b-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d0b-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95d0b-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d0b-180">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="95d0b-180">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="95d0b-181">IDelaydC:: Configure</span><span class="sxs-lookup"><span data-stu-id="95d0b-181">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="95d0b-182">IDelaydC::D la connessione</span><span class="sxs-lookup"><span data-stu-id="95d0b-182">IDelaydC::Disconnect</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="95d0b-183">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="95d0b-183">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> </dl>

 

 




