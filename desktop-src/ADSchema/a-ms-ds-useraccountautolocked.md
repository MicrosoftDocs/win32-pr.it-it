---
title: Attributo ms-DS-User-Account-Auto-Locked
description: Indica se l'account a cui fa riferimento questo attributo è stato bloccato.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- Ms-DS-User-Account-Auto-Locked attribute AD Schema
- Schema AD dell'attributo ms-DS-UserAccountAutoLocked
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1360b9169d5355ef23caf47fa56a283dc4e5267fb603aa08bd0600f126c69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119300301"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>Attributo ms-DS-User-Account-Auto-Locked

Indica se l'account a cui fa riferimento questo attributo è stato bloccato. True se l'account è bloccato; in caso contrario, False.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Auto-Locked       |
| Ldap-Display-Name | ms-DS-UserAccountAutoLocked          |
| Dimensione              | \-                                   |
| Privilegio di aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-Id-Guid    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
| Sintassi            | [**Boolean**](s-boolean.md)         |



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
| System-Flags           | 0x00000014                                                        |
| Classi usate in        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Commenti

In ADAM questo attributo sostituisce il flag [**ADS \_ UF \_ LOCKOUT**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl.**](a-useraccountcontrol.md)

 

