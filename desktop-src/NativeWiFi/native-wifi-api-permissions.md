---
description: Autorizzazioni API WiFi Native
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Autorizzazioni API WiFi Native
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afafec7619e0920a17e3769a430c8c79aeff3828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227394"
---
# <a name="native-wifi-api-permissions"></a><span data-ttu-id="8f211-103">Autorizzazioni API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="8f211-103">Native Wifi API Permissions</span></span>

<span data-ttu-id="8f211-104">Una chiamata API nativa WiFi può avere esito negativo con quando un chiamante non dispone delle autorizzazioni appropriate per eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="8f211-104">A Native Wifi API call may fail with when a caller does not have adequate permissions to perform the requested operation.</span></span>

<span data-ttu-id="8f211-105">Le autorizzazioni vengono archiviate in un elenco di [controllo di accesso discrezionale (DACL)](../secauthz/access-control-lists.md) associato a un [**\_ \_ oggetto a protezione diretta WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span><span class="sxs-lookup"><span data-stu-id="8f211-105">Permissions are stored in a [discretionary access control lists (DACL)](../secauthz/access-control-lists.md) associated with a [**WLAN\_SECURABLE\_OBJECT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span></span> <span data-ttu-id="8f211-106">Per ulteriori informazioni sugli elenchi DACL e gli oggetti a protezione diretta, vedere come gli elenchi [DACL controllano l'accesso a un oggetto](../secauthz/how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="8f211-106">For more information about DACLs and securable objects, see [How DACLs Control Access to an Object](../secauthz/how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="8f211-107">Nella tabella seguente vengono illustrate le funzioni Wi-Fi native che utilizzano oggetti a protezione diretta per determinare se il chiamante dispone di autorizzazioni sufficienti per eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="8f211-107">The following table shows the Native Wifi functions that use securable objects to determine if the caller has sufficient permissions to perform the requested operation.</span></span> <span data-ttu-id="8f211-108">Mostra anche gli oggetti a protezione diretta usati da ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="8f211-108">It also shows the securable objects used by each function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f211-109">Funzione</span><span class="sxs-lookup"><span data-stu-id="8f211-109">Function</span></span></th>
<th><span data-ttu-id="8f211-110">Oggetto a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="8f211-110">Securable object</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f211-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f211-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"><strong>WlanSetFilterList</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="8f211-112">wlan_secure_deny_list</span><span class="sxs-lookup"><span data-stu-id="8f211-112">wlan_secure_deny_list</span></span></li>
<li><span data-ttu-id="8f211-113">wlan_secure_permit_list</span><span class="sxs-lookup"><span data-stu-id="8f211-113">wlan_secure_permit_list</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f211-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f211-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="8f211-115">wlan_secure_ihv_control</span><span class="sxs-lookup"><span data-stu-id="8f211-115">wlan_secure_ihv_control</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f211-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f211-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"><strong>WlanSetAutoConfigParameter</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="8f211-117">wlan_secure_show_denied</span><span class="sxs-lookup"><span data-stu-id="8f211-117">wlan_secure_show_denied</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f211-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f211-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"><strong>WlanSetInterface</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="8f211-119">wlan_secure_ac_enabled</span><span class="sxs-lookup"><span data-stu-id="8f211-119">wlan_secure_ac_enabled</span></span></li>
<li><span data-ttu-id="8f211-120">wlan_secure_bc_scan_enabled</span><span class="sxs-lookup"><span data-stu-id="8f211-120">wlan_secure_bc_scan_enabled</span></span></li>
<li><span data-ttu-id="8f211-121">wlan_secure_bss_type</span><span class="sxs-lookup"><span data-stu-id="8f211-121">wlan_secure_bss_type</span></span></li>
<li><span data-ttu-id="8f211-122">wlan_secure_current_operation_mode</span><span class="sxs-lookup"><span data-stu-id="8f211-122">wlan_secure_current_operation_mode</span></span></li>
<li><span data-ttu-id="8f211-123">wlan_secure_interface_properties</span><span class="sxs-lookup"><span data-stu-id="8f211-123">wlan_secure_interface_properties</span></span></li>
<li><span data-ttu-id="8f211-124">wlan_secure_media_streaming_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="8f211-124">wlan_secure_media_streaming_mode_enabled</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f211-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f211-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="8f211-126">wlan_secure_add_new_all_user_profiles</span><span class="sxs-lookup"><span data-stu-id="8f211-126">wlan_secure_add_new_all_user_profiles</span></span></li>
<li><span data-ttu-id="8f211-127">wlan_secure_add_new_per_user_profiles</span><span class="sxs-lookup"><span data-stu-id="8f211-127">wlan_secure_add_new_per_user_profiles</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f211-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f211-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"><strong>WlanSetProfilePosition</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="8f211-129">wlan_secure_all_user_profiles_order</span><span class="sxs-lookup"><span data-stu-id="8f211-129">wlan_secure_all_user_profiles_order</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8f211-130">Prima che una delle funzioni con nome precedente completi l'operazione, la funzione recupera l'elenco DACL archiviato nell'oggetto a protezione diretta appropriato.</span><span class="sxs-lookup"><span data-stu-id="8f211-130">Before one of the above-named functions completes its operation, the function retrieves the DACL stored in the appropriate securable object.</span></span> <span data-ttu-id="8f211-131">La funzione quindi controlla l'elenco DACL per verificare se il chiamante dispone di autorizzazioni sufficienti.</span><span class="sxs-lookup"><span data-stu-id="8f211-131">The function then checks the DACL to see if the caller has sufficient permissions.</span></span> <span data-ttu-id="8f211-132">Per le \* funzioni WlanGet e WlanQuery \* è necessario che l'elenco DACL includa una [voce di controllo di accesso (ACE)](../secauthz/access-control-entries.md) che concede il [token di accesso](../secauthz/access-tokens.md) dell' \_ accesso in lettura WLAN al thread chiamante \_ alla funzione.</span><span class="sxs-lookup"><span data-stu-id="8f211-132">The WlanGet\* and WlanQuery\* functions require that the DACL contains an [access control entry (ACE)](../secauthz/access-control-entries.md) that grants the [access token](../secauthz/access-tokens.md) of the calling thread WLAN\_READ\_ACCESS to the function.</span></span> <span data-ttu-id="8f211-133">Le \* funzioni WlanSet richiedono una voce ACE che concede il token di accesso dell'accesso in scrittura alla rete WLAN del thread chiamante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8f211-133">The WlanSet\* functions require an ACE that grants the access token of the calling thread WLAN\_WRITE\_ACCESS.</span></span> <span data-ttu-id="8f211-134">Se il chiamante non dispone di autorizzazioni sufficienti, la chiamata di funzione ha esito negativo e viene negato l'errore di \_ accesso \_ .</span><span class="sxs-lookup"><span data-stu-id="8f211-134">If the caller does not have sufficient permissions, the function call fails with the error ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="8f211-135">Per impostazione predefinita, a ogni oggetto a protezione diretta è associato un DACL.</span><span class="sxs-lookup"><span data-stu-id="8f211-135">Each securable object has a DACL associated with it by default.</span></span> <span data-ttu-id="8f211-136">Le autorizzazioni predefinite archiviate nell'elenco DACL possono essere modificate tramite la funzione [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) .</span><span class="sxs-lookup"><span data-stu-id="8f211-136">The default permissions stored in the DACL can be changed using the [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) function.</span></span> <span data-ttu-id="8f211-137">Per determinare i diritti utente validi necessari per eseguire un'operazione su un particolare sistema, chiamare [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="8f211-137">To determine the effective user rights required to perform an operation on a particular system, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="8f211-138">Tutti i profili utente hanno autorizzazioni aggiuntive associate al profilo stesso.</span><span class="sxs-lookup"><span data-stu-id="8f211-138">All-user profiles have additional permissions associated with the profile itself.</span></span> <span data-ttu-id="8f211-139">Le autorizzazioni per un profilo utente totale vengono stabilite quando il profilo viene creato o modificato tramite [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) o [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span><span class="sxs-lookup"><span data-stu-id="8f211-139">The permissions on an all-user profile are established when the profile is created or modified using [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) or [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span></span> <span data-ttu-id="8f211-140">Il parametro *strAllUserProfileSecurity* specifica le autorizzazioni necessarie per la modifica di un profilo, l'eliminazione di un profilo o la connessione a una rete usando un profilo.</span><span class="sxs-lookup"><span data-stu-id="8f211-140">The *strAllUserProfileSecurity* parameter specifies the required permissions for modifying a profile, deleting a profile, or connecting to a network using a profile.</span></span> <span data-ttu-id="8f211-141">Per eliminare o modificare un profilo è necessario disporre delle \_ autorizzazioni di accesso in scrittura WLAN \_ .</span><span class="sxs-lookup"><span data-stu-id="8f211-141">Deleting or modifying a profile requires WLAN\_WRITE\_ACCESS permission.</span></span> <span data-ttu-id="8f211-142">Per la connessione a una rete con un profilo è necessario disporre delle \_ autorizzazioni di accesso WLAN Execute \_ .</span><span class="sxs-lookup"><span data-stu-id="8f211-142">Connecting to a network using a profile requires WLAN\_EXECUTE\_ACCESS permission.</span></span>

<span data-ttu-id="8f211-143">\* \* Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2: \* \* le funzioni [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) e [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="8f211-143">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* The [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) and [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) functions are not supported.</span></span> <span data-ttu-id="8f211-144">Il parametro *strAllUserProfileSecurity* non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8f211-144">The *strAllUserProfileSecurity* parameter is not used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f211-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f211-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f211-146">Come gli elenchi DACL controllano l'accesso a un oggetto</span><span class="sxs-lookup"><span data-stu-id="8f211-146">How DACLs Control Access to an Object</span></span>](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="8f211-147">**\_oggetto a protezione diretta WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="8f211-147">**WLAN\_SECURABLE\_OBJECT**</span></span>](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
