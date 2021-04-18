---
description: È possibile utilizzare i metodi dell'oggetto SWbemLocator per ottenere un oggetto SWbemServices che rappresenta una connessione a uno spazio dei nomi in un computer locale o in un computer host remoto.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Oggetto SWbemLocator (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313174"
---
# <a name="swbemlocator-object"></a><span data-ttu-id="bc86c-103">Oggetto SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="bc86c-103">SWbemLocator object</span></span>

<span data-ttu-id="bc86c-104">È possibile utilizzare i metodi dell'oggetto **SWbemLocator** per ottenere un oggetto [**SWbemServices**](swbemservices.md) che rappresenta una connessione a uno spazio dei nomi in un computer locale o in un computer host remoto.</span><span class="sxs-lookup"><span data-stu-id="bc86c-104">You can use the methods of the **SWbemLocator** object to obtain an [**SWbemServices**](swbemservices.md) object that represents a connection to a namespace on either a local computer or a remote host computer.</span></span> <span data-ttu-id="bc86c-105">È quindi possibile utilizzare i metodi dell'oggetto **SWbemServices** per accedere a WMI.</span><span class="sxs-lookup"><span data-stu-id="bc86c-105">You can then use the methods of the **SWbemServices** object to access WMI.</span></span> <span data-ttu-id="bc86c-106">Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="bc86c-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="bc86c-107">Membri</span><span class="sxs-lookup"><span data-stu-id="bc86c-107">Members</span></span>

<span data-ttu-id="bc86c-108">L'oggetto **SWbemLocator** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bc86c-108">The **SWbemLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="bc86c-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc86c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc86c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc86c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc86c-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc86c-111">Methods</span></span>

<span data-ttu-id="bc86c-112">L'oggetto **SWbemLocator** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bc86c-112">The **SWbemLocator** object has these methods.</span></span>



| <span data-ttu-id="bc86c-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="bc86c-113">Method</span></span>                                              | <span data-ttu-id="bc86c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc86c-114">Description</span></span>                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="bc86c-115">**ConnectServer**</span><span class="sxs-lookup"><span data-stu-id="bc86c-115">**ConnectServer**</span></span>](swbemlocator-connectserver.md) | <span data-ttu-id="bc86c-116">Stabilisce la connessione a WMI nel computer specificato.</span><span class="sxs-lookup"><span data-stu-id="bc86c-116">Connects to WMI on the specified computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bc86c-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc86c-117">Properties</span></span>

<span data-ttu-id="bc86c-118">L'oggetto **SWbemLocator** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc86c-118">The **SWbemLocator** object has these properties.</span></span>



| <span data-ttu-id="bc86c-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc86c-119">Property</span></span>                                                | <span data-ttu-id="bc86c-120">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="bc86c-120">Access type</span></span>          | <span data-ttu-id="bc86c-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc86c-121">Description</span></span>                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="bc86c-122">**Sicurezza\_**</span><span class="sxs-lookup"><span data-stu-id="bc86c-122">**Security\_**</span></span>](swbemlocator-security-.md)<br/> | <span data-ttu-id="bc86c-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc86c-123">Read-only</span></span><br/> | <span data-ttu-id="bc86c-124">Utilizzato per leggere o modificare le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bc86c-124">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc86c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc86c-125">Remarks</span></span>

<span data-ttu-id="bc86c-126">Nella parte superiore del modello a oggetti della libreria di scripting WMI è l'oggetto SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="bc86c-126">At the top of the WMI scripting library object model is the SWbemLocator object.</span></span> <span data-ttu-id="bc86c-127">SWbemLocator viene utilizzato per stabilire una connessione autenticata a uno spazio dei nomi WMI, molto come la funzione GetObject di VBScript e il moniker WMI "winmgmts:" vengono utilizzati per stabilire una connessione autenticata a WMI.</span><span class="sxs-lookup"><span data-stu-id="bc86c-127">SWbemLocator is used to establish an authenticated connection to a WMI namespace, much as the VBScript GetObject function and the WMI moniker "winmgmts:" are used to establish an authenticated connection to WMI.</span></span> <span data-ttu-id="bc86c-128">Tuttavia, SWbemLocator è progettato per risolvere due scenari di scripting specifici che non possono essere eseguiti tramite GetObject e il moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="bc86c-128">However, SWbemLocator is designed to address two specific scripting scenarios that cannot be performed using GetObject and the WMI moniker.</span></span> <span data-ttu-id="bc86c-129">È necessario usare SWbemLocator se è necessario:</span><span class="sxs-lookup"><span data-stu-id="bc86c-129">You must use SWbemLocator if you need to:</span></span>

-   <span data-ttu-id="bc86c-130">Fornire le credenziali utente e password per la connessione a WMI in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="bc86c-130">Provide user and password credentials to connect to WMI on a remote computer.</span></span> <span data-ttu-id="bc86c-131">Il moniker WMI utilizzato con la funzione GetObject non include un meccanismo per specificare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="bc86c-131">The WMI moniker used with the GetObject function does not include a mechanism for specifying credentials.</span></span> <span data-ttu-id="bc86c-132">Per la maggior parte delle attività WMI, incluse tutte quelle eseguite su computer remoti, sono necessari i diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="bc86c-132">Most WMI activities (including all of those carried out on remote computers) require administrator rights.</span></span> <span data-ttu-id="bc86c-133">Se in genere si accede con un account utente normale invece che con un account amministratore, non sarà possibile eseguire la maggior parte delle attività WMI, a meno che non si esegua lo script con credenziali alternative.</span><span class="sxs-lookup"><span data-stu-id="bc86c-133">If you typically log on using a regular user account instead of an administrator account, you will not be able to perform most WMI tasks unless you run the script under alternate credentials.</span></span>
-   <span data-ttu-id="bc86c-134">Connettersi a WMI se si esegue uno script WMI dall'interno di una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="bc86c-134">Connect to WMI if you are running a WMI script from within a Web page.</span></span> <span data-ttu-id="bc86c-135">Non è possibile usare la funzione GetObject quando si eseguono script incorporati all'interno di una pagina HTML perché Internet Explorer non consente l'uso di GetObject per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bc86c-135">You cannot use the GetObject function when running scripts embedded within an HTML page because Internet Explorer disallows the use of GetObject for security reasons.</span></span>

<span data-ttu-id="bc86c-136">Inoltre, è possibile utilizzare SWbemLocator per connettersi a WMI se si individua la stringa di connessione WMI utilizzata con la funzionalità GetObject confusa o complessa.</span><span class="sxs-lookup"><span data-stu-id="bc86c-136">In addition, you might want to use SWbemLocator to connect to WMI if you find the WMI connection string used with GetObject confusing or difficult.</span></span>

<span data-ttu-id="bc86c-137">Usare CreateObject anziché GetObject per creare un riferimento a SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="bc86c-137">You use CreateObject rather than GetObject to create a reference to SWbemLocator.</span></span> <span data-ttu-id="bc86c-138">Per creare il riferimento, è necessario passare la funzione CreateObject SWbemLocator programmatical Identifier (ProgID) "WbemScripting. SWbemLocator", come illustrato nella riga 2 dello script di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="bc86c-138">To create the reference, you must pass the CreateObject function the SWbemLocator programmatic identifier (ProgID) "WbemScripting.SWbemLocator", as shown on line 2 in the following script sample.</span></span> <span data-ttu-id="bc86c-139">Dopo aver ottenuto un riferimento a un oggetto SWbemLocator, chiamare il metodo ConnectServer per connettersi a WMI e ottenere un riferimento a un oggetto SWbemServices.</span><span class="sxs-lookup"><span data-stu-id="bc86c-139">After you obtain a reference to an SWbemLocator object, you call the ConnectServer method to connect to WMI and obtain a reference to an SWbemServices object.</span></span> <span data-ttu-id="bc86c-140">Questa operazione viene illustrata nella riga 3 dello script seguente.</span><span class="sxs-lookup"><span data-stu-id="bc86c-140">This is demonstrated on line 3 of the following script.</span></span>


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="bc86c-141">Per eseguire uno script con credenziali alternative, includere il nome utente e la password come parametri aggiuntivi passati a ConnectServer.</span><span class="sxs-lookup"><span data-stu-id="bc86c-141">To run a script under alternate credentials, include the user name and password as additional parameters passed to ConnectServer.</span></span> <span data-ttu-id="bc86c-142">Ad esempio, questo script viene eseguito con le credenziali di un utente denominato kenmyer, con la password HomerJ.</span><span class="sxs-lookup"><span data-stu-id="bc86c-142">For example, this script runs under the credentials of a user named kenmyer, with the password homerj.</span></span>


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="bc86c-143">È anche possibile usare il \\ formato del nome utente di dominio per specificare un nome utente.</span><span class="sxs-lookup"><span data-stu-id="bc86c-143">You can also use the Domain\\User Name format to specify a user name.</span></span> <span data-ttu-id="bc86c-144">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="bc86c-144">For example:</span></span>

`" fabrikam\kenmyer"`

## <a name="examples"></a><span data-ttu-id="bc86c-145">Esempi</span><span class="sxs-lookup"><span data-stu-id="bc86c-145">Examples</span></span>

<span data-ttu-id="bc86c-146">L'esempio di PowerShell seguente usa **SWbemLocator** per connettersi a un server.</span><span class="sxs-lookup"><span data-stu-id="bc86c-146">The following PowerShell example uses **SWbemLocator** to connect to a server.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="bc86c-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc86c-147">Requirements</span></span>



| <span data-ttu-id="bc86c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc86c-148">Requirement</span></span> | <span data-ttu-id="bc86c-149">Valore</span><span class="sxs-lookup"><span data-stu-id="bc86c-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc86c-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc86c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="bc86c-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc86c-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc86c-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc86c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="bc86c-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc86c-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc86c-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc86c-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc86c-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc86c-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc86c-156">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bc86c-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc86c-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc86c-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc86c-158">DLL</span><span class="sxs-lookup"><span data-stu-id="bc86c-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc86c-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc86c-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc86c-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="bc86c-160">CLSID</span></span><br/>                    | <span data-ttu-id="bc86c-161">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="bc86c-161">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="bc86c-162">IID</span><span class="sxs-lookup"><span data-stu-id="bc86c-162">IID</span></span><br/>                      | <span data-ttu-id="bc86c-163">\_ISWBEMLOCATOR IID</span><span class="sxs-lookup"><span data-stu-id="bc86c-163">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="bc86c-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc86c-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc86c-165">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="bc86c-165">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




