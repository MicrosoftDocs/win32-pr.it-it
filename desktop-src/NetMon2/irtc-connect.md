---
description: 'Metodo IRTC::Connect: il metodo Connect connette il protocollo NPP alla rete usando una scheda di interfaccia di rete specificata e fornisce informazioni di configurazione per la connessione.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: Metodo IRTC::Connect (Netmon.h)
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
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110745"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="17b2d-103">Metodo IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="17b2d-103">IRTC::Connect method</span></span>

<span data-ttu-id="17b2d-104">Il **metodo Connect** connette il NPP alla rete usando una scheda di interfaccia di rete specificata e fornisce informazioni di configurazione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="17b2d-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b2d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17b2d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="17b2d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17b2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b2d-107">*hInputBlob* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17b2d-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b2d-108">Handle al BLOB che specifica la scheda di interfaccia di rete a cui ci si connette e le informazioni di configurazione per tale connessione.</span><span class="sxs-lookup"><span data-stu-id="17b2d-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="17b2d-109">*StatusCallbackProc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17b2d-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b2d-110">Indirizzo della funzione di callback dello stato dell'utente, che riceve gli aggiornamenti dello stato, ad esempio i trigger.</span><span class="sxs-lookup"><span data-stu-id="17b2d-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="17b2d-111">Questo parametro può essere impostato su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="17b2d-112">*FramesCallbackProc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17b2d-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b2d-113">Indirizzo della funzione di callback dei frame dell'utente, usata per ricevere gli aggiornamenti dello stato, ad esempio i trigger.</span><span class="sxs-lookup"><span data-stu-id="17b2d-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="17b2d-114">Questo parametro può essere impostato su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="17b2d-115">*Oggetto UserContext* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17b2d-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b2d-116">Valore passato quando viene chiamata la funzione di callback dello stato e del frame dell'utente.</span><span class="sxs-lookup"><span data-stu-id="17b2d-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="17b2d-117">Se vengono specificate entrambe le funzioni di callback, devono usare lo stesso valore del contesto utente.</span><span class="sxs-lookup"><span data-stu-id="17b2d-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="17b2d-118">Il valore di questo parametro è in genere HWND o un puntatore 'this'.</span><span class="sxs-lookup"><span data-stu-id="17b2d-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="17b2d-119">*hErrorBlob* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="17b2d-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17b2d-120">Handle a un BLOB di errore che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="17b2d-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="17b2d-121">Per informazioni sugli elementi presenti nel BLOB degli errori, vedere la sezione Osservazioni alla fine di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="17b2d-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b2d-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17b2d-122">Return value</span></span>

<span data-ttu-id="17b2d-123">Se questo metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="17b2d-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="17b2d-124">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti ,che includono gli errori restituiti dalla chiamata **interna IRTC::Configure:**</span><span class="sxs-lookup"><span data-stu-id="17b2d-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="17b2d-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="17b2d-125">Return code</span></span>                                                                                                         | <span data-ttu-id="17b2d-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17b2d-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17b2d-127"><dt>**NMERR \_ GIÀ \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="17b2d-128">Questa istanza dell'oggetto COM NPP è già connessa alla rete.</span><span class="sxs-lookup"><span data-stu-id="17b2d-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="17b2d-129"><dt>**ERRORE DI \_ \_ CONVERSIONE BLOB \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="17b2d-130">Il BLOB di configurazione è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="17b2d-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="17b2d-131">Questo errore viene generato dalla chiamata **IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="17b2d-132"><dt>**LA VOCE BLOB NMERR \_ \_ NON \_ \_ \_ ESISTE**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="17b2d-133">Il BLOB di input specificato dal *parametro hInputBlob* non dispone di una voce necessaria per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="17b2d-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="17b2d-134">Questo errore può essere generato dalla chiamata **IRTC::Connect** o **IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="17b2d-135">Esaminare il BLOB di errore restituito *da hErrorBlob* per determinare quale voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="17b2d-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="17b2d-136"><dt>**BLOB NMERR \_ \_ NON \_ INIZIALIZZATO**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="17b2d-137">La **funzione CreateBlob** non è stata chiamata.</span><span class="sxs-lookup"><span data-stu-id="17b2d-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="17b2d-138">Questo errore viene generato dalla chiamata **IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="17b2d-139"><dt>**STRINGA BLOB NMERR \_ \_ NON \_ VALIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="17b2d-140">La stringa non è con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="17b2d-140">The string is not null-terminated.</span></span> <span data-ttu-id="17b2d-141">Questo errore viene generato dalla chiamata **IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="17b2d-142"><dt>**TRIGGER NMERR \_ NON \_ VALIDO**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="17b2d-143">La parte trigger del BLOB di input è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="17b2d-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="17b2d-144">Questo errore viene generato dalla chiamata **IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="17b2d-145"><dt>**BLOB NON VALIDO DI NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="17b2d-146">L'oggetto specificato in *hInputBlob* non è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="17b2d-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="17b2d-147">Questo errore viene generato dalla **chiamata IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="17b2d-148"><dt>**MEMORIA INSUFFICIENTE \_ DI NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="17b2d-149">La memoria necessaria per eseguire questa operazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="17b2d-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="17b2d-150">Questo errore viene generato dalla **chiamata IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="17b2d-151"><dt>**NMERR \_ TIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="17b2d-152">Timeout della richiesta. Questo errore viene generato dalla **chiamata IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="17b2d-153"><dt>**BLOB DI \_ LIVELLO SUPERIORE NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="17b2d-154">Il numero di versione del BLOB specificato in *hInputBlob* non è corretto.</span><span class="sxs-lookup"><span data-stu-id="17b2d-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="17b2d-155">Questo errore viene generato dalla **chiamata IRTC::Configure.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="17b2d-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="17b2d-156">Remarks</span></span>

<span data-ttu-id="17b2d-157">Quando viene chiamato il metodo **Connect,** il NPP chiama automaticamente il metodo **IRTC::Configure** usando il BLOB fornito da *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="17b2d-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="17b2d-158">Si noti che tutti i codici di errore restituiti dalla chiamata a **IRTC::Configure** vengono passati e restituiti dalla **chiamata ARTC::Connect.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="17b2d-159">Questo metodo deve essere chiamato prima di poter avviare l'acquisizione dei frame.</span><span class="sxs-lookup"><span data-stu-id="17b2d-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="17b2d-160">Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare **l'interfaccia IRTC** per acquisire i frame.</span><span class="sxs-lookup"><span data-stu-id="17b2d-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="17b2d-161">Quando si chiama questa funzione, è necessario specificare una funzione di callback di stato o frame, anche se funge solo da segnaposto.</span><span class="sxs-lookup"><span data-stu-id="17b2d-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="17b2d-162">Il BLOB di input specificato da *hInputBlob* può essere ottenuto chiamando i metodi **GetNPPBlobFromUI,** **GetNPPBlobTable** e **SelectNPPBlobFromTable.**</span><span class="sxs-lookup"><span data-stu-id="17b2d-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="17b2d-163">Il BLOB di errore restituito in *hErrorBlob contiene* informazioni sull'errore che possono essere usate dallo sviluppatore o dall'applicazione per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="17b2d-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="17b2d-164">Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non sono in grado di comprendere o trovare nel BLOB di input specificato in *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="17b2d-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="17b2d-165">Ad esempio, se viene restituito NMERR BLOB ENTRY DOES NOT EXIST, la voce Network Monitor impossibile trovare è inclusa nel \_ \_ BLOB di errore \_ \_ \_ restituito.</span><span class="sxs-lookup"><span data-stu-id="17b2d-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="17b2d-166">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="17b2d-166">For information about</span></span>                          | <span data-ttu-id="17b2d-167">Vedere</span><span class="sxs-lookup"><span data-stu-id="17b2d-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="17b2d-168">Recupero del BLOB di input che rappresenta una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="17b2d-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="17b2d-169">Selezione di una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="17b2d-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="17b2d-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17b2d-170">Requirements</span></span>



| <span data-ttu-id="17b2d-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b2d-171">Requirement</span></span> | <span data-ttu-id="17b2d-172">Valore</span><span class="sxs-lookup"><span data-stu-id="17b2d-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b2d-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17b2d-173">Minimum supported client</span></span><br/> | <span data-ttu-id="17b2d-174">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17b2d-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="17b2d-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17b2d-175">Minimum supported server</span></span><br/> | <span data-ttu-id="17b2d-176">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17b2d-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="17b2d-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17b2d-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="17b2d-178"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="17b2d-179">DLL</span><span class="sxs-lookup"><span data-stu-id="17b2d-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17b2d-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b2d-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b2d-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17b2d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b2d-182">IRTC</span><span class="sxs-lookup"><span data-stu-id="17b2d-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="17b2d-183">IRTC::Configure</span><span class="sxs-lookup"><span data-stu-id="17b2d-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="17b2d-184">IRTC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="17b2d-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="17b2d-185">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="17b2d-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




