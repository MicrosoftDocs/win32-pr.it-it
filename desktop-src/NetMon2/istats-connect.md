---
description: Il metodo Connect connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione per la connessione.
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'Metodo IStats:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7705600c3ce68b719014c928ac4d02c62cba64cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885846"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="028e1-103">IStats:: Connect (metodo)</span><span class="sxs-lookup"><span data-stu-id="028e1-103">IStats::Connect method</span></span>

<span data-ttu-id="028e1-104">Il metodo **Connect** connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="028e1-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="028e1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="028e1-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="028e1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="028e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="028e1-107">*hInputBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="028e1-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028e1-108">Handle per il BLOB che specifica la scheda di interfaccia di rete a cui si connette l'oggetto NPP e le informazioni di configurazione per tale connessione.</span><span class="sxs-lookup"><span data-stu-id="028e1-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="028e1-109">*StatusCallbackProc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="028e1-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028e1-110">Indirizzo della funzione di callback dell'utente, che riceve gli aggiornamenti di stato, ad esempio i trigger.</span><span class="sxs-lookup"><span data-stu-id="028e1-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="028e1-111">Se non viene utilizzata una funzione di callback, impostare questo parametro e il parametro *userContext* su **null**.</span><span class="sxs-lookup"><span data-stu-id="028e1-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="028e1-112">*UserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="028e1-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028e1-113">Valore passato quando viene chiamata la funzione di callback dell'utente.</span><span class="sxs-lookup"><span data-stu-id="028e1-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="028e1-114">Il valore di questo parametro è in genere HWND o un puntatore ' This '.</span><span class="sxs-lookup"><span data-stu-id="028e1-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="028e1-115">Se non viene specificata una funzione di callback, impostare questo parametro e il parametro *StatusCallbackProc* su **null**.</span><span class="sxs-lookup"><span data-stu-id="028e1-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="028e1-116">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="028e1-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="028e1-117">Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="028e1-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="028e1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="028e1-118">Return value</span></span>

<span data-ttu-id="028e1-119">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="028e1-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="028e1-120">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti (che includono gli errori restituiti dalla chiamata Internal **IStats:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="028e1-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="028e1-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="028e1-121">Return code</span></span></th>
<th><span data-ttu-id="028e1-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="028e1-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="028e1-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-124">Questa istanza dell'oggetto COM NPP è già connessa alla rete.</span><span class="sxs-lookup"><span data-stu-id="028e1-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="028e1-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-126">Il BLOB di configurazione è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="028e1-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="028e1-127">Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="028e1-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-129">Il BLOB di input specificato dal parametro <em>hInputBlob</em> non dispone di una voce necessaria per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="028e1-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="028e1-130">Questo errore potrebbe essere generato dalla chiamata <strong>IStats:: Connect</strong> o <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="028e1-131">Esaminare il BLOB di errore restituito da <em>hErrorBlob</em> per determinare quale voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="028e1-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="028e1-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-133">La funzione <strong>CreateBlob</strong> non è stata chiamata.</span><span class="sxs-lookup"><span data-stu-id="028e1-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="028e1-134">Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="028e1-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-136">La stringa non termina con null.</span><span class="sxs-lookup"><span data-stu-id="028e1-136">The string is not null-terminated.</span></span> <span data-ttu-id="028e1-137">Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="028e1-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-139">La parte del trigger del BLOB di input è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="028e1-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="028e1-140">Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="028e1-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-142">L'oggetto specificato in <em>hInputBlob</em> non è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="028e1-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="028e1-143">Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="028e1-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-145">La directory di acquisizione predefinita non è stata impostata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="028e1-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="028e1-146">Per impostare la directory di acquisizione, utilizzare il percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="028e1-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="028e1-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-148">La memoria necessaria per eseguire questa operazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="028e1-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="028e1-149">Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="028e1-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-151">Timeout della richiesta. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="028e1-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="028e1-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="028e1-153">Il numero di versione del BLOB specificato in <em>hInputBlob</em> non è corretto.</span><span class="sxs-lookup"><span data-stu-id="028e1-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="028e1-154">Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="028e1-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="028e1-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="028e1-155">Remarks</span></span>

<span data-ttu-id="028e1-156">Quando viene chiamato il metodo **Connect** , Network Monitor chiama automaticamente il metodo **IStats:: Configure** usando il BLOB fornito dal parametro *hInputBlob* .</span><span class="sxs-lookup"><span data-stu-id="028e1-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="028e1-157">Si noti che qualsiasi codice di errore restituito dalla chiamata a **IStats:: Configure** viene passato nuovamente e restituito dalla chiamata **IStats:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="028e1-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="028e1-158">Questo metodo deve essere chiamato prima che sia possibile avviare l'acquisizione di frame.</span><span class="sxs-lookup"><span data-stu-id="028e1-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="028e1-159">Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare l'interfaccia **IStats** per acquisire i frame.</span><span class="sxs-lookup"><span data-stu-id="028e1-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="028e1-160">Il BLOB di input specificato da *hInputBlob* può essere ottenuto chiamando i metodi **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable** .</span><span class="sxs-lookup"><span data-stu-id="028e1-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="028e1-161">Il BLOB di errori restituito dal parametro *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di input specificato in *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="028e1-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="028e1-162">Il BLOB di errori restituito contiene informazioni sugli errori che possono essere utilizzate dall'applicazione per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="028e1-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="028e1-163">Se, ad esempio, \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce che Network Monitor non è stata trovata è inclusa nel BLOB di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="028e1-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="028e1-164">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="028e1-164">For information about</span></span>                                             | <span data-ttu-id="028e1-165">Vedere</span><span class="sxs-lookup"><span data-stu-id="028e1-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="028e1-166">Recupero del BLOB di input che rappresenta una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="028e1-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="028e1-167">Selezione di una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="028e1-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="028e1-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="028e1-168">Requirements</span></span>



| <span data-ttu-id="028e1-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="028e1-169">Requirement</span></span> | <span data-ttu-id="028e1-170">Valore</span><span class="sxs-lookup"><span data-stu-id="028e1-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="028e1-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="028e1-171">Minimum supported client</span></span><br/> | <span data-ttu-id="028e1-172">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="028e1-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="028e1-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="028e1-173">Minimum supported server</span></span><br/> | <span data-ttu-id="028e1-174">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="028e1-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="028e1-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="028e1-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="028e1-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="028e1-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="028e1-177">DLL</span><span class="sxs-lookup"><span data-stu-id="028e1-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="028e1-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="028e1-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="028e1-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="028e1-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="028e1-180">IStats</span><span class="sxs-lookup"><span data-stu-id="028e1-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="028e1-181">IStats:: Configure</span><span class="sxs-lookup"><span data-stu-id="028e1-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="028e1-182">IStats::D la connessione</span><span class="sxs-lookup"><span data-stu-id="028e1-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="028e1-183">BLOB Network Monitor</span><span class="sxs-lookup"><span data-stu-id="028e1-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




