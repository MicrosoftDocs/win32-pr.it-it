---
title: attributo ms-DS-user-Encrypted-text-password-allowed
description: Indica se Active Directory la password viene archiviata nel formato di crittografia reversibile.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- ms-DS-utente-crittografato-testo-password-schema AD attributo consentito
- Schema AD dell'attributo ms-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479760"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>attributo ms-DS-user-Encrypted-text-password-allowed

Indica se Active Directory la password viene archiviata nel formato di crittografia reversibile. True se la password è archiviata nel formato di crittografia reversibile; in caso contrario, false.

> [!Note]  
> Questo attributo non viene usato da [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) ed è incluso solo per la completezza e la parità con userAccountControl. AD LDS non archivia le password con la crittografia reversibile, indipendentemente dal valore di questo attributo per un determinato oggetto o dai criteri di sicurezza del computer che riguardano la crittografia reversibile nel computer stesso.

 



| Voce | Valore |
|-------------------|--------------------------------------------|
| CN                | ms-DS-utente-crittografato-testo-password-consentito |
| LDAP-Display-Name | ms-DS-UserEncryptedTextPasswordAllowed     |
| Dimensione              | \-                                         |
| Privilegio aggiornamento  | \-                                         |
| Frequenza di aggiornamento  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-ID-GUID    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Sintassi            | [**Boolean**](s-boolean.md)               |



## <a name="implementations"></a>Implementazioni

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|-------------------------------------------------------------------|
| ID collegamento                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| È a valore singolo       | Vero                                                              |
| Indicizzato             | Falso                                                             |
| Nel catalogo globale      | Falso                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classi utilizzate in        | [**ms-DS-associabile-oggetto**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Commenti

In ADAM, questo attributo sostituisce il flag [**Ads \_ UF \_ Encrypted \_ Text \_ password \_ consentita**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl**](a-useraccountcontrol.md) .

 

