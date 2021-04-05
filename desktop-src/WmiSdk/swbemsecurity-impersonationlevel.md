---
description: La proprietà ImpersonationLevel è un numero intero che definisce il livello di rappresentazione COM assegnato a questo oggetto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Proprietà SWbemSecurity. ImpersonationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885386"
---
# <a name="swbemsecurityimpersonationlevel-property"></a><span data-ttu-id="213dc-103">Proprietà SWbemSecurity. ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="213dc-103">SWbemSecurity.ImpersonationLevel property</span></span>

<span data-ttu-id="213dc-104">La proprietà **ImpersonationLevel** è un numero intero che definisce il livello di rappresentazione com assegnato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="213dc-104">The **ImpersonationLevel** property is an integer that defines the COM impersonation level that is assigned to this object.</span></span> <span data-ttu-id="213dc-105">Questa impostazione determina se i processi di proprietà di Strumentazione gestione Windows (WMI) possono rilevare o utilizzare le credenziali di sicurezza quando si effettuano chiamate ad altri processi.</span><span class="sxs-lookup"><span data-stu-id="213dc-105">This setting determines if processes owned by Windows Management Instrumentation (WMI) can detect or use your security credentials when making calls to other processes.</span></span> <span data-ttu-id="213dc-106">Per ulteriori informazioni sui livelli di rappresentazione, vedere [impostazione della \_ sicurezza del \_ processo dell'applicazione client](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="213dc-106">For more information about impersonation levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span>

<span data-ttu-id="213dc-107">Se non si imposta il livello di rappresentazione in modo specifico in un moniker o se si imposta la proprietà **SWBemSecurity. ImpersonationLevel** su un oggetto a protezione diretta, WMI imposta il livello di rappresentazione predefinito sul valore specificato nella [chiave del registro di sistema del livello di rappresentazione predefinito](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="213dc-107">If you do not set the impersonation level specifically in either a moniker, or by setting the **SWBemSecurity.ImpersonationLevel** property on a securable object, WMI sets the default impersonation level to the value specified in the [default impersonation level registry key](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="213dc-108">Se questa impostazione non è sufficiente, il provider non esegue la manutenzione della richiesta e la chiamata all'API WMI può avere esito negativo con codice di errore **wbemErrAccessDenied** (2147749891/0x80041003).</span><span class="sxs-lookup"><span data-stu-id="213dc-108">If this setting is not sufficient, the provider does not service your request, and the call to the WMI API can fail with an error code of **wbemErrAccessDenied** (2147749891/0x80041003).</span></span>

<span data-ttu-id="213dc-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="213dc-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="213dc-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="213dc-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="213dc-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="213dc-111">Syntax</span></span>


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="213dc-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="213dc-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="213dc-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="213dc-113">Remarks</span></span>

<span data-ttu-id="213dc-114">Come livello di rappresentazione DCOM, questa proprietà può essere impostata su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="213dc-114">As a DCOM impersonation level, this property can be set to one of the following values:</span></span>



| <span data-ttu-id="213dc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="213dc-115">Value</span></span>           | <span data-ttu-id="213dc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="213dc-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="213dc-117">**Anonimo**</span><span class="sxs-lookup"><span data-stu-id="213dc-117">**Anonymous**</span></span>   | <span data-ttu-id="213dc-118">Nasconde le credenziali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="213dc-118">Hides the credentials of the caller.</span></span> <span data-ttu-id="213dc-119">WMI non supporta effettivamente questo livello di rappresentazione; Se uno script specifica impersonationLevel = Anonymous, WMI aggiornerà automaticamente il livello di rappresentazione per identificare.</span><span class="sxs-lookup"><span data-stu-id="213dc-119">WMI does not actually support this impersonation level; if a script specifies impersonationLevel=Anonymous, WMI will silently upgrade the impersonation level to Identify.</span></span> <span data-ttu-id="213dc-120">In alcuni casi, tuttavia, un esercizio non significativo, perché gli script che usano il livello di identificazione avranno probabilmente esito negativo.</span><span class="sxs-lookup"><span data-stu-id="213dc-120">This is in some ways a meaningless exercise, however, because scripts using the Identify level are likely to fail.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="213dc-121">**Identificare**</span><span class="sxs-lookup"><span data-stu-id="213dc-121">**Identify**</span></span>    | <span data-ttu-id="213dc-122">Consente agli oggetti di eseguire query sulle credenziali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="213dc-122">Enables objects to query the credentials of the caller.</span></span> <span data-ttu-id="213dc-123">Gli script che usano questo livello di rappresentazione avranno probabilmente esito negativo; il livello di identificazione generalmente non consente di controllare gli elenchi di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="213dc-123">Scripts using this impersonation level are likely to fail; the Identify level typically lets you do no more than check access control lists.</span></span> <span data-ttu-id="213dc-124">Non sarà possibile eseguire script su computer remoti tramite l'operazione di identificazione.</span><span class="sxs-lookup"><span data-stu-id="213dc-124">You will not be able to run scripts against remote computers using Identify.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="213dc-125">**Impersonate**</span><span class="sxs-lookup"><span data-stu-id="213dc-125">**Impersonate**</span></span> | <span data-ttu-id="213dc-126">Consente agli oggetti di usare le credenziali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="213dc-126">Enables objects to use the credentials of the caller.</span></span> <span data-ttu-id="213dc-127">Si consiglia di utilizzare questo livello di rappresentazione con script WMI.</span><span class="sxs-lookup"><span data-stu-id="213dc-127">It is recommended that you use this impersonation level with WMI scripts.</span></span> <span data-ttu-id="213dc-128">Quando si esegue questa operazione, lo script WMI utilizzerà le credenziali dell'utente. di conseguenza, sarà in grado di eseguire tutte le attività che è possibile eseguire.</span><span class="sxs-lookup"><span data-stu-id="213dc-128">When you do so, the WMI script will use your user credentials; as a result, it will be able to perform any tasks that you are able to perform.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="213dc-129">**Delegato**</span><span class="sxs-lookup"><span data-stu-id="213dc-129">**Delegate**</span></span>    | <span data-ttu-id="213dc-130">Consente agli oggetti di permettere ad altri oggetti di usare le credenziali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="213dc-130">Enables objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="213dc-131">La delega consente a uno script di usare le credenziali in un computer remoto e quindi consente a tale computer remoto di usare le credenziali in un altro computer remoto.</span><span class="sxs-lookup"><span data-stu-id="213dc-131">Delegation allows a script to use your credentials on a remote computer and then enables that remote computer to use your credentials on another remote computer.</span></span> <span data-ttu-id="213dc-132">Sebbene sia possibile utilizzare questo livello di rappresentazione all'interno di script WMI, è consigliabile eseguire questa operazione solo se necessario, perché potrebbe causare un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="213dc-132">While you can use this impersonation level within WMI scripts, you should do so only if necessary because it might pose a security risk.</span></span><br/> <span data-ttu-id="213dc-133">Non è possibile utilizzare il livello di rappresentazione del delegato a meno che tutti gli account utente e gli account computer utilizzati nella transazione non siano stati contrassegnati come trusted per la delega in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="213dc-133">You cannot use the Delegate impersonation level unless all the user accounts and computer accounts involved in the transaction have all been marked as Trusted for delegation in Active Directory.</span></span> <span data-ttu-id="213dc-134">Questo consente di ridurre al minimo i rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="213dc-134">This helps minimize the security risks.</span></span> <span data-ttu-id="213dc-135">Sebbene un computer remoto possa utilizzare le proprie credenziali, questa operazione può essere eseguita solo se entrambi i computer interessati dalla transazione sono attendibili per la delega.</span><span class="sxs-lookup"><span data-stu-id="213dc-135">Although a remote computer can use your credentials, it can do so only if both it and any other computers involved in the transaction are trusted for delegation.</span></span><br/> |



 

<span data-ttu-id="213dc-136">Come indicato, la rappresentazione anonima nasconde le credenziali e l'identificazione consente a un oggetto remoto di eseguire query sulle credenziali, ma l'oggetto remoto non può rappresentare il contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="213dc-136">As noted, Anonymous impersonation hides your credentials and Identify permits a remote object to query your credentials, but the remote object cannot impersonate your security context.</span></span> <span data-ttu-id="213dc-137">In altre parole, anche se l'oggetto remoto sa chi è, non può essere "finta". Gli script WMI che accedono a computer remoti utilizzando una di queste due impostazioni in genere avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="213dc-137">(In other words, although the remote object knows who you are, it cannot "pretend" to be you.) WMI scripts accessing remote computers using one of these two settings will generally fail.</span></span> <span data-ttu-id="213dc-138">In realtà, la maggior parte degli script eseguiti nel computer locale utilizzando una di queste due impostazioni avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="213dc-138">In fact, most scripts run on the local computer using one of these two settings will also fail.</span></span>

<span data-ttu-id="213dc-139">La rappresentazione consente al servizio WMI remoto di utilizzare il contesto di sicurezza per eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="213dc-139">Impersonate permits the remote WMI service to use your security context to perform the requested operation.</span></span> <span data-ttu-id="213dc-140">Una richiesta WMI remota che utilizza l'impostazione rappresenta in genere ha esito positivo, purché le credenziali dispongano di privilegi sufficienti per eseguire l'operazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="213dc-140">A remote WMI request that uses the Impersonate setting typically succeeds, provided your credentials have sufficient privileges to perform the intended operation.</span></span> <span data-ttu-id="213dc-141">In altre parole, non è possibile utilizzare WMI per eseguire un'azione (in remoto o in altro modo) che non si dispone delle autorizzazioni necessarie per eseguire all'esterno di WMI.</span><span class="sxs-lookup"><span data-stu-id="213dc-141">In other words, you cannot use WMI to perform an action (remotely or otherwise) that you do not have permission to perform outside WMI.</span></span>

<span data-ttu-id="213dc-142">L'impostazione di impersonationLevel su Delegate consente al servizio WMI remoto di passare le credenziali ad altri oggetti ed è in genere considerato un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="213dc-142">Setting impersonationLevel to Delegate permits the remote WMI service to pass your credentials on to other objects and is generally considered a security risk.</span></span>

<span data-ttu-id="213dc-143">È possibile impostare il livello di rappresentazione di un oggetto [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) impostando la proprietà **ImpersonationLevel** sul valore desiderato.</span><span class="sxs-lookup"><span data-stu-id="213dc-143">You can set the impersonation level of an [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) object by setting the **ImpersonationLevel** property to the desired value.</span></span> <span data-ttu-id="213dc-144">Nell'esempio seguente viene illustrato come impostare il livello di rappresentazione per un oggetto **SWbemObject** :</span><span class="sxs-lookup"><span data-stu-id="213dc-144">The following example shows you how to set the impersonation level for an **SWbemObject** object:</span></span>


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



<span data-ttu-id="213dc-145">È inoltre possibile specificare livelli di rappresentazione come parte di un moniker.</span><span class="sxs-lookup"><span data-stu-id="213dc-145">You can also specify impersonation levels as part of a moniker.</span></span> <span data-ttu-id="213dc-146">Nell'esempio seguente viene impostato il livello di autenticazione e il livello di rappresentazione e viene recuperata un'istanza del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="213dc-146">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a><span data-ttu-id="213dc-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="213dc-147">Requirements</span></span>



| <span data-ttu-id="213dc-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="213dc-148">Requirement</span></span> | <span data-ttu-id="213dc-149">Valore</span><span class="sxs-lookup"><span data-stu-id="213dc-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="213dc-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="213dc-150">Minimum supported client</span></span><br/> | <span data-ttu-id="213dc-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="213dc-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="213dc-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="213dc-152">Minimum supported server</span></span><br/> | <span data-ttu-id="213dc-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="213dc-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="213dc-154">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="213dc-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="213dc-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="213dc-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="213dc-156">DLL</span><span class="sxs-lookup"><span data-stu-id="213dc-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="213dc-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="213dc-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="213dc-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="213dc-158">CLSID</span></span><br/>                    | <span data-ttu-id="213dc-159">\_SWBEMSECURITY CLSID</span><span class="sxs-lookup"><span data-stu-id="213dc-159">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="213dc-160">IID</span><span class="sxs-lookup"><span data-stu-id="213dc-160">IID</span></span><br/>                      | <span data-ttu-id="213dc-161">\_ISWBEMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="213dc-161">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="213dc-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="213dc-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="213dc-163">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="213dc-163">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="213dc-164">Impostazione della \_ sicurezza del processo dell'applicazione client \_</span><span class="sxs-lookup"><span data-stu-id="213dc-164">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="213dc-165">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="213dc-165">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

