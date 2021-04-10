---
title: attributo ms-DS-user-dont-expire-password
description: Indica se la password per l'account a cui fa riferimento questo attributo scadrà.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- ms-DS-user-dont-expire-schema AD dell'attributo password
- attributo msDS-UserDontExpirePassword-schema AD
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122495"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>attributo ms-DS-user-dont-expire-password

Indica se la password per l'account a cui fa riferimento questo attributo scadrà. True se la password non scadrà. in caso contrario, false.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-utente-dont-expire-password      |
| LDAP-Display-Name | msDS-UserDontExpirePassword          |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-ID-GUID    | 8788193a-2925-43d9-a221-bb7fff397675 |
| Sintassi            | [**Boolean**](s-boolean.md)         |



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

In ADAM, questo attributo sostituisce il flag del [**\_ passwd ADS UF \_ dont \_ expire \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl**](a-useraccountcontrol.md) .

 

