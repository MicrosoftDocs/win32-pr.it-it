---
title: Attributo ms-DS-User-Encrypted-Text-Password-Allowed
description: Indica se Active Directory archivierà la password nel formato di crittografia reversibile.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-User-Encrypted-Text-Password-Allowed
- Schema AD dell'attributo ms-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fc10b3facce4bef7cc5ff73abe9e901f67171dc2615b79c62355ac61a7c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118687002"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>Attributo ms-DS-User-Encrypted-Text-Password-Allowed

Indica se Active Directory archivierà la password nel formato di crittografia reversibile. True se la password viene archiviata nel formato di crittografia reversibile. in caso contrario, False.

> [!Note]  
> Questo attributo non viene usato da [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) ed è incluso solo per completezza/parità con userAccountControl. AD LDS non archivia le password con crittografia reversibile, indipendentemente dal valore di questo attributo su un determinato oggetto o i criteri di sicurezza del computer relativi alla crittografia reversibile nel computer stesso.

 



| Voce | Valore |
|-------------------|--------------------------------------------|
| CN                | ms-DS-User-Encrypted-Text-Password-Allowed |
| Ldap-Display-Name | ms-DS-UserEncryptedTextPasswordAllowed     |
| Dimensione              | \-                                         |
| Privilegio di aggiornamento  | \-                                         |
| Frequenza di aggiornamento  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-Id-Guid    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Sintassi            | [**Boolean**](s-boolean.md)               |



## <a name="implementations"></a>Implementazioni

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|-------------------------------------------------------------------|
| ID collegamento                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Is-Single-Valued       | Vero                                                              |
| Indicizzato             | Falso                                                             |
| Nel catalogo globale      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classi usate in        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Commenti

In ADAM questo attributo sostituisce il flag [**ADS \_ UF \_ ENCRYPTED \_ TEXT PASSWORD \_ \_ ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl.**](a-useraccountcontrol.md)

 

