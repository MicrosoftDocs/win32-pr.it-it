---
title: Oggetto ConnectionOptions (WSManDisp. h)
description: L'oggetto ConnectionOptions viene passato al metodo CreateSession per fornire il nome utente e la password associati all'account locale nel computer remoto.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto ConnectionOptions
- Oggetto ConnectionOptions Gestione remota Windows, descritto
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301956"
---
# <a name="connectionoptions-object"></a><span data-ttu-id="72d04-105">Oggetto ConnectionOptions</span><span class="sxs-lookup"><span data-stu-id="72d04-105">ConnectionOptions object</span></span>

<span data-ttu-id="72d04-106">L'oggetto **ConnectionOptions** viene passato al metodo [**CreateSession**](wsman-createsession.md) per fornire il nome utente e la password associati all'account locale nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="72d04-106">The **ConnectionOptions** object is passed to the [**CreateSession**](wsman-createsession.md) method to provide the user name and password associated with the local account on the remote computer.</span></span> <span data-ttu-id="72d04-107">Se non viene fornito alcun parametro, le credenziali dell'account che esegue lo script vengono impostate sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="72d04-107">If no parameters are supplied, then the credentials of the account running the script are set to the default values.</span></span>

## <a name="members"></a><span data-ttu-id="72d04-108">Membri</span><span class="sxs-lookup"><span data-stu-id="72d04-108">Members</span></span>

<span data-ttu-id="72d04-109">L'oggetto **ConnectionOptions** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="72d04-109">The **ConnectionOptions** object has these types of members:</span></span>

-   [<span data-ttu-id="72d04-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72d04-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72d04-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72d04-111">Properties</span></span>

<span data-ttu-id="72d04-112">L'oggetto **ConnectionOptions** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="72d04-112">The **ConnectionOptions** object has these properties.</span></span>



| <span data-ttu-id="72d04-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72d04-113">Property</span></span>                                                  | <span data-ttu-id="72d04-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="72d04-114">Access type</span></span>           | <span data-ttu-id="72d04-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72d04-115">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72d04-116">**Password**</span><span class="sxs-lookup"><span data-stu-id="72d04-116">**Password**</span></span>](connectionoptions-password.md)<br/> | <span data-ttu-id="72d04-117">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="72d04-117">Write-only</span></span><br/> | <span data-ttu-id="72d04-118">Imposta la password di un account locale o di dominio nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="72d04-118">Sets the password of a local or domain account on the remote computer.</span></span><br/>           |
| [<span data-ttu-id="72d04-119">**Nome utente**</span><span class="sxs-lookup"><span data-stu-id="72d04-119">**UserName**</span></span>](connectionoptions-username.md)<br/> | <span data-ttu-id="72d04-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="72d04-120">Read/write</span></span><br/> | <span data-ttu-id="72d04-121">Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="72d04-121">Sets and gets the user name of a local or domain account on the remote computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72d04-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="72d04-122">Remarks</span></span>

<span data-ttu-id="72d04-123">L'oggetto **ConnectionOptions** corrisponde all'interfaccia [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="72d04-123">The **ConnectionOptions** object corresponds to the [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) interface.</span></span>

<span data-ttu-id="72d04-124">Se un'applicazione client Gestione remota Windows viene eseguita con la rappresentazione, si verifica un errore se si imposta la proprietà [**password**](connectionoptions-password.md) .</span><span class="sxs-lookup"><span data-stu-id="72d04-124">If a Windows Remote Management client application is running under impersonation, then a failure occurs if you set the [**Password**](connectionoptions-password.md) property.</span></span> <span data-ttu-id="72d04-125">Un'applicazione client è uno script o un altro programma che invia una richiesta a WinRM nel computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="72d04-125">A client application is a script or other program that sends a request to WinRM on the local or a remote computer.</span></span> <span data-ttu-id="72d04-126">È possibile che l'applicazione client sia in esecuzione con la rappresentazione perché è stata chiamata funzione come [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72d04-126">The client application may be running under impersonation because it called a function like [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span></span> <span data-ttu-id="72d04-127">Una pagina Active Server (ASP) o un servizio non può richiedere un nome utente e una password se il processo ASP viene eseguito con un account che rappresenta un client.</span><span class="sxs-lookup"><span data-stu-id="72d04-127">An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.</span></span>

<span data-ttu-id="72d04-128">Il flag **WSManFlagCredUserNamePassword** deve essere impostato sulla chiamata [**WSMan. CreateSession**](wsman-createsession.md) quando si usano il [**nome utente**](connectionoptions-username.md) e la [**password**](connectionoptions-password.md) per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="72d04-128">The **WSManFlagCredUserNamePassword** flag should be set on the [**WSman.CreateSession**](wsman-createsession.md) call when using the [**UserName**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md) for authentication.</span></span>

## <a name="examples"></a><span data-ttu-id="72d04-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="72d04-129">Examples</span></span>

<span data-ttu-id="72d04-130">Nell'esempio di codice VBScript seguente viene illustrato come creare un oggetto **ConnectionOptions** , impostare le proprietà per l'account nel computer remoto e utilizzarlo per creare un oggetto [**sessione**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="72d04-130">The following VBScript code example shows how to create a **ConnectionOptions** object, set the properties for the account on the remote computer, and use it in creating a [**Session**](session.md) object.</span></span>


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a><span data-ttu-id="72d04-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72d04-131">Requirements</span></span>



| <span data-ttu-id="72d04-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="72d04-132">Requirement</span></span> | <span data-ttu-id="72d04-133">Valore</span><span class="sxs-lookup"><span data-stu-id="72d04-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d04-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72d04-134">Minimum supported client</span></span><br/> | <span data-ttu-id="72d04-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72d04-135">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="72d04-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72d04-136">Minimum supported server</span></span><br/> | <span data-ttu-id="72d04-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72d04-137">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="72d04-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72d04-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d04-139"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d04-139"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72d04-140">IDL</span><span class="sxs-lookup"><span data-stu-id="72d04-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72d04-141"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72d04-141"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="72d04-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="72d04-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="72d04-143"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72d04-143"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72d04-144">DLL</span><span class="sxs-lookup"><span data-stu-id="72d04-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72d04-145"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d04-145"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72d04-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72d04-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d04-147">Autenticazione per le connessioni remote</span><span class="sxs-lookup"><span data-stu-id="72d04-147">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="72d04-148">API di scripting WinRM</span><span class="sxs-lookup"><span data-stu-id="72d04-148">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="72d04-149">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="72d04-149">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="72d04-150">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="72d04-150">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="72d04-151">Creazione di script in Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="72d04-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="72d04-152">Recupero di dati dal computer locale</span><span class="sxs-lookup"><span data-stu-id="72d04-152">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="72d04-153">Recupero di dati da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="72d04-153">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

