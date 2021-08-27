---
title: Attributo User-Account-Control
description: Flag che controllano il comportamento dell'account utente.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo User-Account-Control
- Schema AD dell'attributo userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76ab64d0d93ce7523c3d91d6f4a3ebb5f4d200f0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468798"
---
# <a name="user-account-control-attribute"></a>Attributo User-Account-Control

Flag che controllano il comportamento dell'account utente.



| Voce | valore |
|-------------------|---------------------------------------|
| CN                | Controllo dell'account utente                  |
| Ldap-Display-Name | userAccountControl                    |
| Dimensione              | 4 byte.                              |
| Aggiorna privilegio  | Questo valore viene impostato dal sistema.      |
| Frequenza di aggiornamento  | Ogni volta che i criteri dell'account cambiano. |
| Attribute-Id      | 1.2.840.113556.1.4.8                  |
| System-Id-Guid    | bf967a68-0de6-11d0-a285-00aa003049e2  |
| Sintassi            | [**Enumerazione**](s-enumeration.md)  |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| A valore singolo       | Vero                              |
| Indicizzato             | Vero                              |
| Nel catalogo globale      | Vero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| A valore singolo       | Vero                              |
| Indicizzato             | Vero                              |
| Nel catalogo globale      | Vero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| A valore singolo       | Vero                              |
| Indicizzato             | Vero                              |
| Nel catalogo globale      | Vero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Vero                              |
| Nel catalogo globale      | Vero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Vero                              |
| Nel catalogo globale      | Vero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Vero                              |
| Nel catalogo globale      | Vero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="remarks"></a>Commenti

Il valore di questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.




| Valore esadecimale | Identificatore (definito in iads.h) | Descrizione | 
|-------------------|--------------------------------|-------------|
| 0x00000001 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a> | Viene eseguito lo script di accesso. | 
| 0x00000002 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a> | L'account utente è disabilitato. | 
| 0x00000008 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a> | La home directory è obbligatoria. | 
| 0x00000010 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a> | L'account è attualmente bloccato. | 
| 0x00000020 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a> | Non è necessaria alcuna password. | 
| 0x00000040 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a> | L'utente non può modificare la password.<blockquote>[!Note]<br />Non è possibile assegnare le impostazioni di autorizzazione PASSWD_CANT_CHANGE modificando direttamente l'attributo UserAccountControl. Per altre informazioni e un esempio di codice che illustra come impedire a un utente di modificare la password, vedere <a href="/windows/desktop/ADSI/user-cannot-change-password">L'utente non può modificare la password</a>.</blockquote><br /> : | 
| 0x00000080 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a> | L'utente può inviare una password crittografata. | 
| 0x00000100 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a> | Si tratta di un account per gli utenti il cui account primario si trova in un altro dominio. Questo account fornisce l'accesso utente a questo dominio, ma non a qualsiasi dominio che considera attendibile questo dominio. Noto anche come account utente locale. | 
| 0x00000200 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a> | Si tratta di un tipo di account predefinito che rappresenta un utente tipico. | 
| 0x00000800 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a> | Si tratta di un'autorizzazione per considerare attendibile l'account per un dominio di sistema che considera attendibili altri domini. | 
| 0x00001000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a> | Si tratta di un account computer per un computer membro di questo dominio. | 
| 0x00002000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a> | Si tratta di un account computer per un controller di dominio di backup del sistema membro di questo dominio. | 
| 0x00004000 | N/A | Non usato. | 
| 0x00008000 | N/A | Non usato. | 
| 0x00010000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a> | La password per questo account non scadrà mai. | 
| 0x00020000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a> | Si tratta di un account di accesso MNS. | 
| 0x00040000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a> | L'utente deve accedere usando un smart card. | 
| 0x00080000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a> | L'account del servizio (account utente o computer), con cui viene eseguito un servizio, è attendibile per la delega Kerberos. Qualsiasi servizio di questo tipo può rappresentare un client che richiede il servizio. | 
| 0x00100000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a> | Il contesto di sicurezza dell'utente non verrà delegato a un servizio anche se l'account del servizio è impostato come attendibile per la delega Kerberos. | 
| 0x00200000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a> | Limitare questa entità in modo che usi solo i tipi di crittografia DES (Data Encryption Standard) per le chiavi. | 
| 0x00400000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a> | Questo account non richiede la pre-autenticazione Kerberos per l'accesso. | 
| 0x00800000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a> | La password utente è scaduta. Questo flag viene creato dal sistema usando i dati dell'attributo <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> e dei criteri di dominio. | 
| 0x01000000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a> | L'account è abilitato per la delega. Si tratta di un'impostazione sensibile alla sicurezza. Gli account con questa opzione abilitata devono essere rigorosamente controllati. Questa impostazione consente a un servizio in esecuzione nell'account di presupporre un'identità client ed eseguire l'autenticazione come utente in altri server remoti della rete. | 




 

