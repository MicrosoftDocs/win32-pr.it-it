---
title: ms-DS-user-account-attributo disabilitato
description: Indica se un account è disabilitato o abilitato.
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- Schema di AD per l'attributo ms-DS-user-account-disabled
- attributo msDS-UserAccountDisabled-schema AD
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a01c0b83599a8d6309f6639b94f5d0321180df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480344"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>ms-DS-user-account-attributo disabilitato

Indica se un account è disabilitato o abilitato. True se l'account è disabilitato; in caso contrario, false.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-user-account-disabilitato          |
| LDAP-Display-Name | msDS-UserAccountDisabled             |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| System-ID-GUID    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
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

In ADAM questo attributo sostituisce il flag [**Ads \_ UF \_ ACCOUNTDISABLE**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl**](a-useraccountcontrol.md) .

 

