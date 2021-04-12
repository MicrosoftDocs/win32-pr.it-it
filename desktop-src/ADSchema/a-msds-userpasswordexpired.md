---
title: ms-DS-utente-password-attributo scaduto
description: Indica se la password per l'account a cui fa riferimento questo attributo è scaduta.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-user-password-expired
- attributo msDS-UserPasswordExpired-schema AD
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d99143c470e58d1b1cb5e0cbd7e5302618ff0a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104225281"
---
# <a name="ms-ds-user-password-expired-attribute"></a>ms-DS-utente-password-attributo scaduto

Indica se la password per l'account a cui fa riferimento questo attributo è scaduta. True se la password è scaduta. in caso contrario, false.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-utente-password-scaduto          |
| LDAP-Display-Name | msDS-UserPasswordExpired             |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-ID-GUID    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
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
| System-Flags           | 0x00000014                                                        |
| Classi utilizzate in        | [**ms-DS-associabile-oggetto**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Commenti

In ADAM questo attributo sostituisce il flag [**Ads \_ UF \_ password \_ expired**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl**](a-useraccountcontrol.md) .

 

