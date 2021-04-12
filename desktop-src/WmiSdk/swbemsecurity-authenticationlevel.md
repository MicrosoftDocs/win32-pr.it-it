---
description: La proprietà AuthenticationLevel è un numero intero che definisce il livello di autenticazione COM assegnato a questo oggetto.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Proprietà SWbemSecurity. AuthenticationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344711"
---
# <a name="swbemsecurityauthenticationlevel-property"></a><span data-ttu-id="35948-103">Proprietà SWbemSecurity. AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="35948-103">SWbemSecurity.AuthenticationLevel property</span></span>

<span data-ttu-id="35948-104">La proprietà **AuthenticationLevel** è un numero intero che definisce il livello di autenticazione com assegnato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="35948-104">The **AuthenticationLevel** property is an integer that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="35948-105">Questa impostazione determina la modalità di protezione delle informazioni inviate da WMI.</span><span class="sxs-lookup"><span data-stu-id="35948-105">This setting determines how you protect information sent from WMI.</span></span> <span data-ttu-id="35948-106">Per ulteriori informazioni sui livelli di autenticazione, vedere [impostazione della \_ sicurezza del \_ processo dell'applicazione client](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="35948-106">For more information about authentication levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="35948-107">In generale, non è necessario impostare il livello di autenticazione quando si effettuano chiamate API WMI.</span><span class="sxs-lookup"><span data-stu-id="35948-107">In general, it is not necessary to set the authentication level when making WMI API calls.</span></span> <span data-ttu-id="35948-108">Se non si imposta questa proprietà, verrà utilizzato il livello di autenticazione COM predefinito per il sistema.</span><span class="sxs-lookup"><span data-stu-id="35948-108">If you do not set this property, the default COM Authentication level for your system is used.</span></span>

<span data-ttu-id="35948-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="35948-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="35948-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="35948-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="35948-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35948-111">Syntax</span></span>


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="35948-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="35948-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="35948-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="35948-113">Remarks</span></span>

<span data-ttu-id="35948-114">L'impostazione authenticationLevel consente di richiedere il livello di autenticazione e privacy DCOM da usare in una connessione.</span><span class="sxs-lookup"><span data-stu-id="35948-114">The authenticationLevel setting enables you to request the level of DCOM authentication and privacy to be used throughout a connection.</span></span> <span data-ttu-id="35948-115">Le impostazioni variano da nessuna autenticazione all'autenticazione crittografata per pacchetto.</span><span class="sxs-lookup"><span data-stu-id="35948-115">Settings range from no authentication to per-packet encrypted authentication.</span></span>



| <span data-ttu-id="35948-116">Valore</span><span class="sxs-lookup"><span data-stu-id="35948-116">Value</span></span>        | <span data-ttu-id="35948-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35948-117">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35948-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="35948-118">None</span></span>         | <span data-ttu-id="35948-119">Non usa alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="35948-119">Does not use any authentication.</span></span> <span data-ttu-id="35948-120">Tutte le impostazioni di sicurezza vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="35948-120">All security settings are ignored.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="35948-121">Predefinito</span><span class="sxs-lookup"><span data-stu-id="35948-121">Default</span></span>      | <span data-ttu-id="35948-122">Usa una negoziazione di sicurezza standard per selezionare un livello di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="35948-122">Uses a standard security negotiation to select an authentication level.</span></span> <span data-ttu-id="35948-123">Si tratta dell'impostazione consigliata, perché il client associato alla transazione verrà negoziato al livello di autenticazione specificato dal server.</span><span class="sxs-lookup"><span data-stu-id="35948-123">This is the recommended setting because the client involved in the transaction will be negotiated to the authentication level specified by the server.</span></span><br/> <span data-ttu-id="35948-124">DCOM non seleziona il valore None durante una sessione di negoziazione.</span><span class="sxs-lookup"><span data-stu-id="35948-124">DCOM will not select the value None during a negotiation session.</span></span><br/> |
| <span data-ttu-id="35948-125">Connessione</span><span class="sxs-lookup"><span data-stu-id="35948-125">Connect</span></span>      | <span data-ttu-id="35948-126">Autentica le credenziali del client solo quando il client tenta di connettersi al server.</span><span class="sxs-lookup"><span data-stu-id="35948-126">Authenticates the credentials of the client only when the client tries to connect to the server.</span></span> <span data-ttu-id="35948-127">Dopo la connessione, non viene eseguito alcun controllo di autenticazione aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="35948-127">After a connection has been made, no additional authentication checks take place.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="35948-128">Chiamata</span><span class="sxs-lookup"><span data-stu-id="35948-128">Call</span></span>         | <span data-ttu-id="35948-129">Autentica le credenziali del client solo all'inizio di ogni chiamata, quando il server riceve la richiesta.</span><span class="sxs-lookup"><span data-stu-id="35948-129">Authenticates the credentials of the client only at the beginning of each call, when the server receives the request.</span></span> <span data-ttu-id="35948-130">Le intestazioni dei pacchetti sono firmate, ma i pacchetti di dati scambiati tra il client e il server non sono firmati né crittografati.</span><span class="sxs-lookup"><span data-stu-id="35948-130">The packet headers are signed, but the data packets exchanged between the client and the server are neither signed nor encrypted.</span></span><br/>                                                     |
| <span data-ttu-id="35948-131">PKT</span><span class="sxs-lookup"><span data-stu-id="35948-131">Pkt</span></span>          | <span data-ttu-id="35948-132">Autentica che tutti i pacchetti di dati vengono ricevuti dal client previsto.</span><span class="sxs-lookup"><span data-stu-id="35948-132">Authenticates that all data packets are received from the expected client.</span></span> <span data-ttu-id="35948-133">Simile a Call; le intestazioni di pacchetto sono firmate ma non crittografate.</span><span class="sxs-lookup"><span data-stu-id="35948-133">Similar to Call; packet headers are signed but not encrypted.</span></span> <span data-ttu-id="35948-134">I pacchetti stessi non sono né firmati né crittografati.</span><span class="sxs-lookup"><span data-stu-id="35948-134">Packets themselves are neither signed nor encrypted.</span></span><br/>                                                                                                               |
| <span data-ttu-id="35948-135">PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="35948-135">PktIntegrity</span></span> | <span data-ttu-id="35948-136">Autentica e verifica che nessuno dei pacchetti di dati trasferiti tra il client e il server sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="35948-136">Authenticates and verifies that none of the data packets transferred between the client and the server have been modified.</span></span> <span data-ttu-id="35948-137">Ogni pacchetto di dati è firmato, assicurando che i pacchetti non siano stati modificati durante il transito.</span><span class="sxs-lookup"><span data-stu-id="35948-137">Every data packet is signed, ensuring that the packets have not been modified during transit.</span></span> <span data-ttu-id="35948-138">Nessuno dei pacchetti di dati è crittografato.</span><span class="sxs-lookup"><span data-stu-id="35948-138">None of the data packets are encrypted.</span></span><br/>                                            |
| <span data-ttu-id="35948-139">Su PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="35948-139">PktPrivacy</span></span>   | <span data-ttu-id="35948-140">Autentica tutti i livelli di rappresentazione precedenti e firma e crittografa ogni pacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="35948-140">Authenticates all previous impersonation levels and signs and encrypts each data packet.</span></span> <span data-ttu-id="35948-141">In questo modo si garantisce che tutte le comunicazioni tra il client e il server siano riservate.</span><span class="sxs-lookup"><span data-stu-id="35948-141">This ensures that all communication between the client and the server is confidential.</span></span><br/>                                                                                                                             |



 

<span data-ttu-id="35948-142">È possibile impostare il livello di autenticazione degli oggetti [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) impostando la proprietà **AuthenticationLevel** sul valore desiderato.</span><span class="sxs-lookup"><span data-stu-id="35948-142">You can set the authentication level of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by setting the **AuthenticationLevel** property to the desired value.</span></span>

<span data-ttu-id="35948-143">Nell'esempio seguente viene illustrato come impostare il livello di autenticazione per un oggetto **SwbemObject** .</span><span class="sxs-lookup"><span data-stu-id="35948-143">The following example shows how to set the authentication level for an **SwbemObject** object.</span></span>


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



<span data-ttu-id="35948-144">È anche possibile specificare i livelli di autenticazione come parte di un moniker.</span><span class="sxs-lookup"><span data-stu-id="35948-144">You can also specify authentication levels as part of a moniker.</span></span> <span data-ttu-id="35948-145">Nell'esempio seguente viene impostato il livello di autenticazione e il livello di rappresentazione e viene recuperata un'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="35948-145">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a><span data-ttu-id="35948-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35948-146">Requirements</span></span>



| <span data-ttu-id="35948-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="35948-147">Requirement</span></span> | <span data-ttu-id="35948-148">Valore</span><span class="sxs-lookup"><span data-stu-id="35948-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35948-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35948-149">Minimum supported client</span></span><br/> | <span data-ttu-id="35948-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35948-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35948-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35948-151">Minimum supported server</span></span><br/> | <span data-ttu-id="35948-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35948-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35948-153">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="35948-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="35948-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35948-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35948-155">DLL</span><span class="sxs-lookup"><span data-stu-id="35948-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35948-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35948-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35948-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="35948-157">CLSID</span></span><br/>                    | <span data-ttu-id="35948-158">\_SWBEMSECURITY CLSID</span><span class="sxs-lookup"><span data-stu-id="35948-158">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="35948-159">IID</span><span class="sxs-lookup"><span data-stu-id="35948-159">IID</span></span><br/>                      | <span data-ttu-id="35948-160">\_ISWBEMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="35948-160">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="35948-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35948-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35948-162">Impostazione della \_ sicurezza del processo dell'applicazione client \_</span><span class="sxs-lookup"><span data-stu-id="35948-162">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="35948-163">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="35948-163">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="35948-164">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="35948-164">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> </dl>

 

