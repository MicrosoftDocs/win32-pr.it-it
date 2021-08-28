---
description: Autorizzazioni per l'API Wi-Fi nativa
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Autorizzazioni per l'API Wi-Fi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da56faac08b40ace46ef1e33c5d5644be87b45c6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480727"
---
# <a name="native-wifi-api-permissions"></a>Autorizzazioni per l'API Wi-Fi nativa

Una chiamata API Wi-Fi nativa potrebbe non riuscire quando un chiamante non dispone delle autorizzazioni appropriate per eseguire l'operazione richiesta.

Le autorizzazioni vengono archiviate in un elenco di controllo di accesso discrezionale [(DACL)](../secauthz/access-control-lists.md) associato a un oggetto [**A PROTEZIONE \_ DIRETTA \_ WLAN.**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object) Per altre informazioni sui DACL e sugli oggetti a protezione diretta, vedere [Come gli oggetti DACL controllano l'accesso a un oggetto](../secauthz/how-dacls-control-access-to-an-object.md).

La tabella seguente illustra le funzioni Wi-Fi native che usano oggetti a protezione diretta per determinare se il chiamante dispone di autorizzazioni sufficienti per eseguire l'operazione richiesta. Mostra anche gli oggetti a protezione diretta usati da ogni funzione.




| Funzione | Oggetto a protezione diretta | 
|----------|------------------|
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a><br /> | <ul><li>wlan_secure_deny_list</li><li>wlan_secure_permit_list</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a><br /> | <ul><li>wlan_secure_ihv_control</li></ul> | 
| <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a><br /> | <ul><li>wlan_secure_show_denied</li></ul> | 
| <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a><br /> | <ul><li>wlan_secure_ac_enabled</li><li>wlan_secure_bc_scan_enabled</li><li>wlan_secure_bss_type</li><li>wlan_secure_current_operation_mode</li><li>wlan_secure_interface_properties</li><li>wlan_secure_media_streaming_mode_enabled</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a><br /> | <ul><li>wlan_secure_add_new_all_user_profiles</li><li>wlan_secure_add_new_per_user_profiles</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a><br /> | <ul><li>wlan_secure_all_user_profiles_order</li></ul> | 




 

Prima che una delle funzioni denominate sopra completi l'operazione, la funzione recupera l'elenco DACL archiviato nell'oggetto a protezione diretta appropriato. La funzione controlla quindi l'elenco DACL per verificare se il chiamante dispone di autorizzazioni sufficienti. Le funzioni WlanGet e WlanQuery richiedono che l'elenco DACL contenga una voce di controllo di accesso \* \* [(ACE)](../secauthz/access-control-entries.md) [](../secauthz/access-tokens.md) che concede il token di accesso del thread chiamante WLAN \_ READ ACCESS alla \_ funzione. Le funzioni WlanSet richiedono una ACE che concede il token di \* accesso del thread chiamante WLAN WRITE \_ \_ ACCESS. Se il chiamante non dispone di autorizzazioni sufficienti, la chiamata di funzione ha esito negativo con l'errore ERROR \_ ACCESS \_ DENIED.

A ogni oggetto a protezione diretta è associato un elenco DACL per impostazione predefinita. Le autorizzazioni predefinite archiviate nell'elenco DACL possono essere modificate usando la [**funzione WlanSetSecuritySettings.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) Per determinare i diritti utente effettivi necessari per eseguire un'operazione in un particolare sistema, chiamare [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Tutti i profili utente hanno autorizzazioni aggiuntive associate al profilo stesso. Le autorizzazioni per un profilo utente vengono stabilite quando il profilo viene creato o modificato tramite [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) o [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile). Il *parametro strAllUserProfileSecurity* specifica le autorizzazioni necessarie per modificare un profilo, eliminare un profilo o connettersi a una rete usando un profilo. L'eliminazione o la modifica di un profilo richiede l'autorizzazione \_ WLAN WRITE \_ ACCESS. La connessione a una rete tramite un profilo richiede l'autorizzazione \_ EXECUTE ACCESS WLAN. \_

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2: ** Le funzioni [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) e [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) non sono supportate. Il *parametro strAllUserProfileSecurity* non viene usato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di controllo dell'accesso a un oggetto da parte degli daCL](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**OGGETTO A \_ PROTEZIONE DIRETTA \_ WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
