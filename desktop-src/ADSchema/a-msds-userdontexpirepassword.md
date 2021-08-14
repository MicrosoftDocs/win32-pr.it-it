---
title: Attributo ms-DS-User-Dont-Expire-Password
description: Indica se la password per l'account a cui fa riferimento questo attributo scadrà.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-User-Dont-Expire-Password
- Schema AD dell'attributo msDS-UserDontExpirePassword
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af661ca1317f7506e5bcdbf611010b0fe4c058d5f1e3f1e5f31b917737a6e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425431"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>Attributo ms-DS-User-Dont-Expire-Password

Indica se la password per l'account a cui fa riferimento questo attributo scadrà. True se la password non scadrà. in caso contrario, False.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Dont-Expire-Password      |
| Ldap-Display-Name | msDS-UserDontExpirePassword          |
| Dimensione              | \-                                   |
| Privilegio di aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-Id-Guid    | 8788193a-2925-43d9-a221-bb7fff397675 |
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
| System-Flags           | 0x00000010                                                        |
| Classi usate in        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Commenti

In ADAM questo attributo sostituisce il flag [**ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl.**](a-useraccountcontrol.md)

 

