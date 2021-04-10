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
# <a name="native-wifi-api-permissions"></a>Autorizzazioni API WiFi Native

Una chiamata API nativa WiFi può avere esito negativo con quando un chiamante non dispone delle autorizzazioni appropriate per eseguire l'operazione richiesta.

Le autorizzazioni vengono archiviate in un elenco di [controllo di accesso discrezionale (DACL)](../secauthz/access-control-lists.md) associato a un [**\_ \_ oggetto a protezione diretta WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object). Per ulteriori informazioni sugli elenchi DACL e gli oggetti a protezione diretta, vedere come gli elenchi [DACL controllano l'accesso a un oggetto](../secauthz/how-dacls-control-access-to-an-object.md).

Nella tabella seguente vengono illustrate le funzioni Wi-Fi native che utilizzano oggetti a protezione diretta per determinare se il chiamante dispone di autorizzazioni sufficienti per eseguire l'operazione richiesta. Mostra anche gli oggetti a protezione diretta usati da ogni funzione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Oggetto a protezione diretta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a><br/></td>
<td><ul>
<li>wlan_secure_deny_list</li>
<li>wlan_secure_permit_list</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ihv_control</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a><br/></td>
<td><ul>
<li>wlan_secure_show_denied</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ac_enabled</li>
<li>wlan_secure_bc_scan_enabled</li>
<li>wlan_secure_bss_type</li>
<li>wlan_secure_current_operation_mode</li>
<li>wlan_secure_interface_properties</li>
<li>wlan_secure_media_streaming_mode_enabled</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a><br/></td>
<td><ul>
<li>wlan_secure_add_new_all_user_profiles</li>
<li>wlan_secure_add_new_per_user_profiles</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a><br/></td>
<td><ul>
<li>wlan_secure_all_user_profiles_order</li>
</ul></td>
</tr>
</tbody>
</table>



 

Prima che una delle funzioni con nome precedente completi l'operazione, la funzione recupera l'elenco DACL archiviato nell'oggetto a protezione diretta appropriato. La funzione quindi controlla l'elenco DACL per verificare se il chiamante dispone di autorizzazioni sufficienti. Per le \* funzioni WlanGet e WlanQuery \* è necessario che l'elenco DACL includa una [voce di controllo di accesso (ACE)](../secauthz/access-control-entries.md) che concede il [token di accesso](../secauthz/access-tokens.md) dell' \_ accesso in lettura WLAN al thread chiamante \_ alla funzione. Le \* funzioni WlanSet richiedono una voce ACE che concede il token di accesso dell'accesso in scrittura alla rete WLAN del thread chiamante \_ \_ . Se il chiamante non dispone di autorizzazioni sufficienti, la chiamata di funzione ha esito negativo e viene negato l'errore di \_ accesso \_ .

Per impostazione predefinita, a ogni oggetto a protezione diretta è associato un DACL. Le autorizzazioni predefinite archiviate nell'elenco DACL possono essere modificate tramite la funzione [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) . Per determinare i diritti utente validi necessari per eseguire un'operazione su un particolare sistema, chiamare [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Tutti i profili utente hanno autorizzazioni aggiuntive associate al profilo stesso. Le autorizzazioni per un profilo utente totale vengono stabilite quando il profilo viene creato o modificato tramite [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) o [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile). Il parametro *strAllUserProfileSecurity* specifica le autorizzazioni necessarie per la modifica di un profilo, l'eliminazione di un profilo o la connessione a una rete usando un profilo. Per eliminare o modificare un profilo è necessario disporre delle \_ autorizzazioni di accesso in scrittura WLAN \_ . Per la connessione a una rete con un profilo è necessario disporre delle \_ autorizzazioni di accesso WLAN Execute \_ .

* * Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2: * * le funzioni [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) e [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) non sono supportate. Il parametro *strAllUserProfileSecurity* non viene utilizzato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come gli elenchi DACL controllano l'accesso a un oggetto](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**\_oggetto a protezione diretta WLAN \_**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
