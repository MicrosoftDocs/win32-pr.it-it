---
title: ms-DS-user-account-attributo con blocco automatico
description: Indica se l'account a cui fa riferimento questo attributo è stato bloccato.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- ms-DS-user-account-schema AD attributo con blocco automatico
- Schema AD dell'attributo ms-DS-UserAccountAutoLocked
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6623a1b348af14fecc8dab41a44439bf2d745bf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104048852"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>ms-DS-user-account-attributo con blocco automatico

Indica se l'account a cui fa riferimento questo attributo è stato bloccato. True se l'account è bloccato; in caso contrario, false.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-user-account-bloccato automaticamente       |
| LDAP-Display-Name | ms-DS-UserAccountAutoLocked          |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-ID-GUID    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
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

In ADAM questo attributo sostituisce il flag [**Ads \_ UF \_ locking**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl**](a-useraccountcontrol.md) .

 

