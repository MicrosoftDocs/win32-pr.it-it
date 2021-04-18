---
description: Il metodo Connect connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione per la connessione.
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'Metodo IRTC:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14e34aeb0be30165aa18ddc7da18028d715be01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306557"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="945af-103">Metodo IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="945af-103">IRTC::Connect method</span></span>

<span data-ttu-id="945af-104">Il metodo **Connect** connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="945af-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="945af-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="945af-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="945af-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="945af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="945af-107">*hInputBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="945af-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945af-108">Handle per il BLOB che specifica la scheda di interfaccia di rete a cui ci si connette e le informazioni di configurazione per tale connessione.</span><span class="sxs-lookup"><span data-stu-id="945af-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="945af-109">*StatusCallbackProc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="945af-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945af-110">Indirizzo della funzione di callback dello stato dell'utente, che riceve gli aggiornamenti di stato, ad esempio i trigger.</span><span class="sxs-lookup"><span data-stu-id="945af-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="945af-111">Questo parametro può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="945af-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="945af-112">*FramesCallbackProc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="945af-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945af-113">Indirizzo della funzione di richiamata frame dell'utente, utilizzata per ricevere aggiornamenti di stato, ad esempio i trigger.</span><span class="sxs-lookup"><span data-stu-id="945af-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="945af-114">Questo parametro può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="945af-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="945af-115">*UserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="945af-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945af-116">Valore passato quando viene chiamata la funzione di callback dello stato e del frame dell'utente.</span><span class="sxs-lookup"><span data-stu-id="945af-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="945af-117">Se vengono specificate entrambe le funzioni di callback, è necessario che utilizzino lo stesso valore del contesto utente.</span><span class="sxs-lookup"><span data-stu-id="945af-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="945af-118">Il valore di questo parametro è in genere HWND o un puntatore ' This '.</span><span class="sxs-lookup"><span data-stu-id="945af-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="945af-119">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="945af-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="945af-120">Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="945af-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="945af-121">Per informazioni sul contenuto del BLOB degli errori, vedere la sezione Osservazioni nella parte inferiore di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="945af-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="945af-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="945af-122">Return value</span></span>

<span data-ttu-id="945af-123">Se questo metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="945af-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="945af-124">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti (che includono gli errori restituiti dalla chiamata interna **IRTC:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="945af-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="945af-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="945af-125">Return code</span></span>                                                                                                         | <span data-ttu-id="945af-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="945af-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="945af-127"><dt>**NMERR \_ già \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="945af-128">Questa istanza dell'oggetto COM NPP è già connessa alla rete.</span><span class="sxs-lookup"><span data-stu-id="945af-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="945af-129"><dt>**\_errore di \_ conversione \_ BLOB NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="945af-130">Il BLOB di configurazione è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="945af-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="945af-131">Questo errore viene generato dalla chiamata **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="945af-132"><dt>**\_la voce del BLOB NMERR non \_ \_ \_ \_ esiste**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="945af-133">Il BLOB di input specificato dal parametro *hInputBlob* non dispone di una voce necessaria per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="945af-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="945af-134">Questo errore può essere generato dalla chiamata **IRTC:: Connect** o **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="945af-135">Esaminare il BLOB di errore restituito da *hErrorBlob* per determinare quale voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="945af-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="945af-136"><dt>**\_BLOB NMERR \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="945af-137">La funzione **CreateBlob** non è stata chiamata.</span><span class="sxs-lookup"><span data-stu-id="945af-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="945af-138">Questo errore viene generato dalla chiamata **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="945af-139"><dt>**\_stringa BLOB \_ NMERR \_ non valida**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="945af-140">La stringa non termina con null.</span><span class="sxs-lookup"><span data-stu-id="945af-140">The string is not null-terminated.</span></span> <span data-ttu-id="945af-141">Questo errore viene generato dalla chiamata **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="945af-142"><dt>**TRIGGER NMERR non \_ valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="945af-143">La parte del trigger del BLOB di input è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="945af-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="945af-144">Questo errore viene generato dalla chiamata **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="945af-145"><dt>**\_BLOB NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="945af-146">L'oggetto specificato in *hInputBlob* non è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="945af-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="945af-147">Questo errore viene generato dalla chiamata **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="945af-148"><dt>**\_ \_ \_ memoria insufficiente NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="945af-149">La memoria necessaria per eseguire questa operazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="945af-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="945af-150">Questo errore viene generato dalla chiamata **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="945af-151"><dt>**\_timeout NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="945af-152">Timeout della richiesta. Questo errore viene generato dalla chiamata **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="945af-153"><dt>**BLOB a livello di NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="945af-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="945af-154">Il numero di versione del BLOB specificato in *hInputBlob* non è corretto.</span><span class="sxs-lookup"><span data-stu-id="945af-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="945af-155">Questo errore viene generato dalla chiamata **IRTC:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="945af-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="945af-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="945af-156">Remarks</span></span>

<span data-ttu-id="945af-157">Quando viene chiamato il metodo **Connect** , l'oggetto NPP chiama automaticamente il metodo **IRTC:: Configure** usando il BLOB fornito da *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="945af-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="945af-158">Si noti che tutti i codici di errore restituiti dalla chiamata a **IRTC:: Configure** vengono passati nuovamente e restituiti dalla chiamata **IRTC:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="945af-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="945af-159">Questo metodo deve essere chiamato prima che sia possibile avviare l'acquisizione di frame.</span><span class="sxs-lookup"><span data-stu-id="945af-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="945af-160">Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare l'interfaccia **IRTC** per acquisire i frame.</span><span class="sxs-lookup"><span data-stu-id="945af-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="945af-161">Quando si chiama questa funzione, è necessario specificare una funzione di callback dello stato o del frame, anche se agisce solo come segnaposto.</span><span class="sxs-lookup"><span data-stu-id="945af-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="945af-162">Il BLOB di input specificato da *hInputBlob* può essere ottenuto chiamando i metodi **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable** .</span><span class="sxs-lookup"><span data-stu-id="945af-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="945af-163">Il BLOB di errori restituito in *hErrorBlob* contiene informazioni sull'errore che lo sviluppatore o l'applicazione può utilizzare per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="945af-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="945af-164">Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di input specificato in *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="945af-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="945af-165">Ad esempio, se \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="945af-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="945af-166">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="945af-166">For information about</span></span>                          | <span data-ttu-id="945af-167">Vedere</span><span class="sxs-lookup"><span data-stu-id="945af-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="945af-168">Recupero del BLOB di input che rappresenta una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="945af-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="945af-169">Selezione di una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="945af-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="945af-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="945af-170">Requirements</span></span>



| <span data-ttu-id="945af-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="945af-171">Requirement</span></span> | <span data-ttu-id="945af-172">Valore</span><span class="sxs-lookup"><span data-stu-id="945af-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="945af-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="945af-173">Minimum supported client</span></span><br/> | <span data-ttu-id="945af-174">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="945af-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="945af-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="945af-175">Minimum supported server</span></span><br/> | <span data-ttu-id="945af-176">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="945af-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="945af-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="945af-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="945af-178"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="945af-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="945af-179">DLL</span><span class="sxs-lookup"><span data-stu-id="945af-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="945af-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="945af-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="945af-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="945af-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945af-182">IRTC</span><span class="sxs-lookup"><span data-stu-id="945af-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="945af-183">IRTC:: Configure</span><span class="sxs-lookup"><span data-stu-id="945af-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="945af-184">IRTC::D la connessione</span><span class="sxs-lookup"><span data-stu-id="945af-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="945af-185">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="945af-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




