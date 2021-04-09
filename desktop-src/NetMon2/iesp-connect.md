---
description: Il metodo Connect connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione relative alla connessione.
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: 'Metodo IESP:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4fc9c88b0eb4671c61f268c5857dceba3dc500f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128330"
---
# <a name="iespconnect-method"></a><span data-ttu-id="85452-103">Metodo IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="85452-103">IESP::Connect method</span></span>

<span data-ttu-id="85452-104">Il metodo **Connect** connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione relative alla connessione.</span><span class="sxs-lookup"><span data-stu-id="85452-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="85452-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85452-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="85452-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85452-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85452-107">*hInputBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85452-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85452-108">Handle per il BLOB che specifica la scheda di interfaccia di rete a cui si connette l'oggetto NPP e le informazioni di configurazione per tale connessione.</span><span class="sxs-lookup"><span data-stu-id="85452-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="85452-109">*StatusCallbackProc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85452-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85452-110">Indirizzo della funzione di callback dell'utente, che riceve gli aggiornamenti di stato, ad esempio i trigger.</span><span class="sxs-lookup"><span data-stu-id="85452-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="85452-111">Se non viene utilizzata una funzione di callback, impostare questo parametro e il parametro *userContext* su **null**.</span><span class="sxs-lookup"><span data-stu-id="85452-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85452-112">*UserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85452-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85452-113">Valore passato quando viene chiamata la funzione di callback dell'utente.</span><span class="sxs-lookup"><span data-stu-id="85452-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="85452-114">Il valore di questo parametro è in genere HWND o un puntatore ' This '.</span><span class="sxs-lookup"><span data-stu-id="85452-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="85452-115">Se non viene specificata una funzione di callback, impostare questo parametro e il parametro *StatusCallbackProc* su **null**.</span><span class="sxs-lookup"><span data-stu-id="85452-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85452-116">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85452-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85452-117">Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="85452-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85452-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85452-118">Return value</span></span>

<span data-ttu-id="85452-119">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="85452-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="85452-120">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti (che includono gli errori restituiti dalla chiamata interna **IESP:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="85452-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IESP::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85452-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="85452-121">Return code</span></span></th>
<th><span data-ttu-id="85452-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85452-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="85452-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-124">Questa istanza dell'oggetto COM NPP è già connessa alla rete.</span><span class="sxs-lookup"><span data-stu-id="85452-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="85452-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-126">Il BLOB di configurazione è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="85452-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="85452-127">Questo errore viene generato dalla chiamata <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-127">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="85452-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-129">Il BLOB di input specificato dal parametro <em>hInputBlob</em> non dispone di una voce necessaria per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="85452-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="85452-130">Questo errore potrebbe essere generato dalla chiamata <strong>IESP:: Connect</strong> o <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-130">This error might be generated by the <strong>IESP::Connect</strong> or <strong>IESP::Configure</strong> call.</span></span> <span data-ttu-id="85452-131">Esaminare il BLOB di errore restituito da <em>hErrorBlob</em> per determinare quale voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="85452-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="85452-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-133">La funzione <strong>CreateBlob</strong> non è stata chiamata.</span><span class="sxs-lookup"><span data-stu-id="85452-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="85452-134">Questo errore viene generato dalla chiamata <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-134">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="85452-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-136">La stringa non termina con null.</span><span class="sxs-lookup"><span data-stu-id="85452-136">The string is not null-terminated.</span></span> <span data-ttu-id="85452-137">Questo errore viene generato dalla chiamata <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-137">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="85452-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-139">La parte del trigger del BLOB di input è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="85452-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="85452-140">Questo errore viene generato dalla chiamata <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-140">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="85452-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-142">L'oggetto specificato in <em>hInputBlob</em> non è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="85452-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="85452-143">Questo errore viene generato dalla chiamata <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-143">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="85452-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-145">La directory di acquisizione predefinita non è stata impostata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="85452-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="85452-146">Usare il percorso seguente per impostare la directory di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="85452-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="85452-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-148">La memoria necessaria per eseguire questa operazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="85452-148">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="85452-149">Questo errore viene generato dalla chiamata <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-149">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="85452-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-151">Timeout della richiesta. Questo errore viene generato dalla chiamata <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-151">The request has timed out. This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="85452-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85452-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85452-153">Il numero di versione del BLOB specificato in <em>hInputBlob</em> non è corretto.</span><span class="sxs-lookup"><span data-stu-id="85452-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="85452-154">Questo errore viene generato dalla chiamata <strong>IESP:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="85452-154">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="85452-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="85452-155">Remarks</span></span>

<span data-ttu-id="85452-156">Quando viene chiamato il metodo **Connect** , Network Monitor chiama automaticamente **IESP:: Configure** usando il BLOB fornito dal parametro *hInputBlob* .</span><span class="sxs-lookup"><span data-stu-id="85452-156">When the **Connect** method is called, Network Monitor automatically calls **IESP::Configure** by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="85452-157">Si noti che tutti i codici di errore restituiti dalla chiamata a **IESP:: Configure** vengono passati nuovamente e restituiti dalla chiamata **IESP:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="85452-157">Note that any error codes returned by the call to **IESP::Configure** are passed back and returned by the **IESP::Connect** call.</span></span>

<span data-ttu-id="85452-158">Questo metodo deve essere chiamato prima che sia possibile avviare l'acquisizione di frame.</span><span class="sxs-lookup"><span data-stu-id="85452-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="85452-159">Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare l'interfaccia **IESP** per acquisire i frame.</span><span class="sxs-lookup"><span data-stu-id="85452-159">Note that when you connect to the network by using this method, you must continue to use the **IESP** interface to capture frames.</span></span>

<span data-ttu-id="85452-160">Il BLOB di input specificato da *hInputBlob* può essere ottenuto chiamando **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable**.</span><span class="sxs-lookup"><span data-stu-id="85452-160">The input BLOB specified by *hInputBlob* can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="85452-161">Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di input specificato in *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="85452-161">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="85452-162">Il BLOB di errori restituito contiene informazioni sugli errori che possono essere utilizzate dall'applicazione per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="85452-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="85452-163">Se, ad esempio, \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce che Network Monitor non è stata trovata è inclusa nel BLOB di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="85452-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="85452-164">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="85452-164">For information about</span></span>                          | <span data-ttu-id="85452-165">Vedere</span><span class="sxs-lookup"><span data-stu-id="85452-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="85452-166">Recupero del BLOB di input che rappresenta una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="85452-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="85452-167">Selezione di una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="85452-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="85452-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85452-168">Requirements</span></span>



| <span data-ttu-id="85452-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="85452-169">Requirement</span></span> | <span data-ttu-id="85452-170">Valore</span><span class="sxs-lookup"><span data-stu-id="85452-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85452-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85452-171">Minimum supported client</span></span><br/> | <span data-ttu-id="85452-172">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85452-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="85452-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85452-173">Minimum supported server</span></span><br/> | <span data-ttu-id="85452-174">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85452-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="85452-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85452-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="85452-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="85452-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="85452-177">DLL</span><span class="sxs-lookup"><span data-stu-id="85452-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85452-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85452-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85452-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85452-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85452-180">IESP</span><span class="sxs-lookup"><span data-stu-id="85452-180">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="85452-181">IESP:: Configure</span><span class="sxs-lookup"><span data-stu-id="85452-181">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="85452-182">IESP::D la connessione</span><span class="sxs-lookup"><span data-stu-id="85452-182">IESP::Disconnect</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="85452-183">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="85452-183">IESP::Start</span></span>](iesp-start.md)
</dt> </dl>

 

 




