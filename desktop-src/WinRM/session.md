---
title: Oggetto Session (WSManDisp. h)
description: Definisce le operazioni e le impostazioni della sessione.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto sessione
- Gestione remota Windows oggetto sessione, descritto
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964972"
---
# <a name="session-object-wsmandisph"></a><span data-ttu-id="2d9b7-105">Oggetto Session (WSManDisp. h)</span><span class="sxs-lookup"><span data-stu-id="2d9b7-105">Session object (WSManDisp.h)</span></span>

<span data-ttu-id="2d9b7-106">Definisce le operazioni e le impostazioni della sessione.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-106">Defines operations and session settings.</span></span> <span data-ttu-id="2d9b7-107">Qualsiasi operazione di Gestione remota Windows richiede la creazione di una **sessione** che si connette a un computer remoto, a un [*controller di gestione di base*](windows-remote-management-glossary.md) (BMC) o al computer locale.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-107">Any Windows Remote Management operations require creation of a **Session** that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="2d9b7-108">Le operazioni di rete WinRM includono il recupero, la scrittura o l'enumerazione dei dati o la chiamata di metodi.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-108">WinRM network operations include getting, writing, or enumerating data, or invoking methods.</span></span> <span data-ttu-id="2d9b7-109">I metodi dell'oggetto **sessione** rispecchiano le operazioni di base definite nel protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-109">The methods of the **Session** object mirror the basic operations defined in the WS-Management protocol.</span></span>

## <a name="members"></a><span data-ttu-id="2d9b7-110">Membri</span><span class="sxs-lookup"><span data-stu-id="2d9b7-110">Members</span></span>

<span data-ttu-id="2d9b7-111">L'oggetto **sessione** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2d9b7-111">The **Session** object has these types of members:</span></span>

-   [<span data-ttu-id="2d9b7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2d9b7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d9b7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d9b7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d9b7-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="2d9b7-114">Methods</span></span>

<span data-ttu-id="2d9b7-115">L'oggetto **Session** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-115">The **Session** object has these methods.</span></span>



| <span data-ttu-id="2d9b7-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="2d9b7-116">Method</span></span>                                 | <span data-ttu-id="2d9b7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d9b7-117">Description</span></span>                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d9b7-118">**Creare**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-118">**Create**</span></span>](session-create.md)       | <span data-ttu-id="2d9b7-119">Crea una nuova istanza di una risorsa e restituisce l'URI del nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-119">Creates a new instance of a resource and returns the URI of the new object.</span></span><br/>                                      |
| [<span data-ttu-id="2d9b7-120">**Delete**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-120">**Delete**</span></span>](session-delete.md)       | <span data-ttu-id="2d9b7-121">Elimina la risorsa specificata nell'URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-121">Deletes the resource specified in the resource URI.</span></span><br/>                                                              |
| [<span data-ttu-id="2d9b7-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-122">**Enumerate**</span></span>](session-enumerate.md) | <span data-ttu-id="2d9b7-123">Enumera un insieme, una tabella o una risorsa del log del messaggio.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-123">Enumerates a collection, table, or message log resource.</span></span><br/>                                                         |
| [<span data-ttu-id="2d9b7-124">**Recupero**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-124">**Get**</span></span>](session-get.md)             | <span data-ttu-id="2d9b7-125">Recupera una risorsa dal servizio e restituisce una rappresentazione XML dell'istanza corrente della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-125">Retrieves a resource from the service and returns an XML representation of the current instance of the resource.</span></span><br/> |
| [<span data-ttu-id="2d9b7-126">**Identificare**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-126">**Identify**</span></span>](session-identify.md)   | <span data-ttu-id="2d9b7-127">Esegue una query su un computer remoto per determinare se supporta il protocollo WS-Management</span><span class="sxs-lookup"><span data-stu-id="2d9b7-127">Queries a remote computer to determine if it supports the WS-Management protocol</span></span><br/>                                 |
| [<span data-ttu-id="2d9b7-128">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-128">**Invoke**</span></span>](session-invoke.md)       | <span data-ttu-id="2d9b7-129">Richiama un metodo che restituisce i risultati della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-129">Invokes a method that returns the results of the method call.</span></span><br/>                                                    |
| [<span data-ttu-id="2d9b7-130">**Mettere**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-130">**Put**</span></span>](session-put.md)             | <span data-ttu-id="2d9b7-131">Aggiorna una risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-131">Updates a resource.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="2d9b7-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d9b7-132">Properties</span></span>

<span data-ttu-id="2d9b7-133">L'oggetto **Session** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-133">The **Session** object has these properties.</span></span>



| <span data-ttu-id="2d9b7-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d9b7-134">Property</span></span>                                            | <span data-ttu-id="2d9b7-135">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2d9b7-135">Access type</span></span>           | <span data-ttu-id="2d9b7-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d9b7-136">Description</span></span>                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d9b7-137">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-137">**BatchItems**</span></span>](session-batchitems.md)<br/> | <span data-ttu-id="2d9b7-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2d9b7-138">Read/write</span></span><br/> | <span data-ttu-id="2d9b7-139">Imposta e ottiene il numero di elementi in ogni batch di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-139">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="2d9b7-140">Questo valore non può essere modificato durante un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-140">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="2d9b7-141">Per impostazione predefinita, il valore predefinito è un numero illimitato di elementi.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-141">By default, the default is an unlimited number of items.</span></span> <span data-ttu-id="2d9b7-142">Il provider di risorse può impostare un limite.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-142">The resource provider may set a limit.</span></span><br/> |
| [<span data-ttu-id="2d9b7-143">**Errore**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-143">**Error**</span></span>](session-error.md)<br/>           | <span data-ttu-id="2d9b7-144">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d9b7-144">Read-only</span></span><br/>  | <span data-ttu-id="2d9b7-145">Ottiene informazioni aggiuntive sull'errore in un flusso XML.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-145">Gets additional error information in an XML stream.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="2d9b7-146">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="2d9b7-146">**Timeout**</span></span>](session-timeout.md)<br/>       | <span data-ttu-id="2d9b7-147">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2d9b7-147">Read/write</span></span><br/> | <span data-ttu-id="2d9b7-148">Imposta e ottiene la quantità massima di tempo (in millisecondi) per l'attesa da parte dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-148">Sets and gets the maximum amount of time (in milliseconds) for the client application to wait.</span></span><br/>                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="2d9b7-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d9b7-149">Remarks</span></span>

<span data-ttu-id="2d9b7-150">L'oggetto **Session** corrisponde all'interfaccia [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) .</span><span class="sxs-lookup"><span data-stu-id="2d9b7-150">The **Session** object corresponds to the [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="2d9b7-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="2d9b7-151">Examples</span></span>

<span data-ttu-id="2d9b7-152">Nell'esempio di codice VBScript riportato di seguito viene illustrato come creare un oggetto **sessione** .</span><span class="sxs-lookup"><span data-stu-id="2d9b7-152">The following VBScript code example shows how to create a **Session** object.</span></span>


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a><span data-ttu-id="2d9b7-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d9b7-153">Requirements</span></span>



| <span data-ttu-id="2d9b7-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d9b7-154">Requirement</span></span> | <span data-ttu-id="2d9b7-155">Valore</span><span class="sxs-lookup"><span data-stu-id="2d9b7-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d9b7-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d9b7-156">Minimum supported client</span></span><br/> | <span data-ttu-id="2d9b7-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d9b7-157">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2d9b7-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d9b7-158">Minimum supported server</span></span><br/> | <span data-ttu-id="2d9b7-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d9b7-159">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2d9b7-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d9b7-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d9b7-161"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d9b7-161"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d9b7-162">IDL</span><span class="sxs-lookup"><span data-stu-id="2d9b7-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d9b7-163"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d9b7-163"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d9b7-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d9b7-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d9b7-165"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2d9b7-165"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2d9b7-166">DLL</span><span class="sxs-lookup"><span data-stu-id="2d9b7-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d9b7-167"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d9b7-167"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d9b7-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d9b7-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9b7-169">API di scripting WinRM</span><span class="sxs-lookup"><span data-stu-id="2d9b7-169">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="2d9b7-170">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="2d9b7-170">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="2d9b7-171">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="2d9b7-171">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="2d9b7-172">Creazione di script in Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="2d9b7-172">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="2d9b7-173">Recupero di dati dal computer locale</span><span class="sxs-lookup"><span data-stu-id="2d9b7-173">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="2d9b7-174">Recupero di dati da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="2d9b7-174">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





