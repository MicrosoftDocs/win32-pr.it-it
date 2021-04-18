---
description: L'oggetto SWbemSecurity Ottiene o imposta le impostazioni di sicurezza, ad esempio i privilegi, le rappresentazioni COM e i livelli di autenticazione assegnati a un oggetto.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Oggetto SWbemSecurity (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309784"
---
# <a name="swbemsecurity-object"></a><span data-ttu-id="0e0e7-103">Oggetto SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="0e0e7-103">SWbemSecurity object</span></span>

<span data-ttu-id="0e0e7-104">L'oggetto **SWbemSecurity** Ottiene o imposta le impostazioni di sicurezza, ad esempio i privilegi, le rappresentazioni com e i livelli di autenticazione assegnati a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-104">The **SWbemSecurity** object gets or sets security settings, such as privileges, COM impersonations, and authentication levels assigned to an object.</span></span> <span data-ttu-id="0e0e7-105">Gli oggetti [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md)e [**SWbemEventSource**](swbemeventsource.md) hanno una proprietà **di \_ sicurezza** , che corrisponde all'oggetto **SWbemSecurity** .</span><span class="sxs-lookup"><span data-stu-id="0e0e7-105">The [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md), and [**SWbemEventSource**](swbemeventsource.md) objects have a **Security\_** property, which is the **SWbemSecurity** object.</span></span> <span data-ttu-id="0e0e7-106">Quando si recupera un'istanza o si Visualizza il registro di protezione WMI, potrebbe essere necessario impostare le proprietà dell'oggetto di **sicurezza \_** .</span><span class="sxs-lookup"><span data-stu-id="0e0e7-106">When you retrieve an instance or view the WMI security log, you might need to set the properties of the **Security\_** object.</span></span>

<span data-ttu-id="0e0e7-107">La chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript non è in grado di creare l'oggetto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-107">The VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call cannot create the Security object.</span></span> <span data-ttu-id="0e0e7-108">Le impostazioni di sicurezza in questo oggetto non identificano le impostazioni di autenticazione, rappresentazione o privilegio in una connessione a WMI oppure la sicurezza attiva per il proxy quando un oggetto viene recapitato a un sink in una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-108">The security settings in this object do not identify the authentication, impersonation, or privilege settings on a connection to WMI, or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="0e0e7-109">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="0e0e7-109">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

## <a name="members"></a><span data-ttu-id="0e0e7-110">Membri</span><span class="sxs-lookup"><span data-stu-id="0e0e7-110">Members</span></span>

<span data-ttu-id="0e0e7-111">L'oggetto **SWbemSecurity** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0e0e7-111">The **SWbemSecurity** object has these types of members:</span></span>

-   [<span data-ttu-id="0e0e7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e0e7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e0e7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e0e7-113">Properties</span></span>

<span data-ttu-id="0e0e7-114">L'oggetto **SWbemSecurity** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-114">The **SWbemSecurity** object has these properties.</span></span>



| <span data-ttu-id="0e0e7-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e0e7-115">Property</span></span>                                                                    | <span data-ttu-id="0e0e7-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="0e0e7-116">Access type</span></span>           | <span data-ttu-id="0e0e7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e0e7-117">Description</span></span>                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e0e7-118">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="0e0e7-118">**AuthenticationLevel**</span></span>](swbemsecurity-authenticationlevel.md)<br/> | <span data-ttu-id="0e0e7-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0e0e7-119">Read/write</span></span><br/> | <span data-ttu-id="0e0e7-120">Valore numerico che definisce il livello di autenticazione COM assegnato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-120">Numeric value that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="0e0e7-121">Questa impostazione determina la modalità di protezione delle informazioni inviate da WMI.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-121">This setting determines how you protect information sent from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="0e0e7-122">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="0e0e7-122">**ImpersonationLevel**</span></span>](swbemsecurity-impersonationlevel.md)<br/>   | <span data-ttu-id="0e0e7-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0e0e7-123">Read/write</span></span><br/> | <span data-ttu-id="0e0e7-124">Valore numerico che definisce il livello di rappresentazione COM assegnato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-124">Numeric value that defines the COM Impersonation level that is assigned to this object.</span></span> <span data-ttu-id="0e0e7-125">Questa impostazione determina se i processi di proprietà di WMI possono rilevare o utilizzare le credenziali di sicurezza quando si effettuano chiamate ad altri processi.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-125">This setting determines if processes owned by WMI can detect or use your security credentials when making calls to other processes.</span></span><br/> |
| [<span data-ttu-id="0e0e7-126">**Privilegi**</span><span class="sxs-lookup"><span data-stu-id="0e0e7-126">**Privileges**</span></span>](swbemsecurity-privileges.md)<br/>                   | <span data-ttu-id="0e0e7-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e0e7-127">Read-only</span></span><br/>  | <span data-ttu-id="0e0e7-128">Oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) che definisce i privilegi per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e0e7-128">An [**SWbemPrivilegeSet**](swbemprivilegeset.md) object that defines privileges for this object.</span></span> <span data-ttu-id="0e0e7-129">Per ulteriori informazioni, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="0e0e7-129">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="0e0e7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e0e7-130">Requirements</span></span>



| <span data-ttu-id="0e0e7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e0e7-131">Requirement</span></span> | <span data-ttu-id="0e0e7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0e0e7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e0e7-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e0e7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0e0e7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e0e7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e0e7-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e0e7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0e0e7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e0e7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e0e7-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e0e7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e0e7-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e0e7-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e0e7-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e0e7-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e0e7-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e0e7-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e0e7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0e0e7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e0e7-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e0e7-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e0e7-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="0e0e7-143">CLSID</span></span><br/>                    | <span data-ttu-id="0e0e7-144">\_SWBEMSECURITY CLSID</span><span class="sxs-lookup"><span data-stu-id="0e0e7-144">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="0e0e7-145">IID</span><span class="sxs-lookup"><span data-stu-id="0e0e7-145">IID</span></span><br/>                      | <span data-ttu-id="0e0e7-146">\_ISWBEMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="0e0e7-146">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="0e0e7-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e0e7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e0e7-148">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="0e0e7-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="0e0e7-149">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="0e0e7-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="0e0e7-150">Impostazione della \_ sicurezza del processo dell'applicazione client \_</span><span class="sxs-lookup"><span data-stu-id="0e0e7-150">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="0e0e7-151">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="0e0e7-151">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="0e0e7-152">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="0e0e7-152">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="0e0e7-153">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="0e0e7-153">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

