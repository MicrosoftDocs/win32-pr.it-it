---
title: ms-DS-utente-password-attributo non obbligatorio
description: Indica se è necessaria una password per l'account a cui fa riferimento questo attributo.
ms.assetid: 86779c6f-d05c-409a-afe4-99ebf7c0593e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-utente-password-non obbligatorio
- Schema AD dell'attributo ms-DS-UserPasswordNotRequired
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Not-Required
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8ebb439af9a960d2dc0721940d9f4d2ab852b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123066"
---
# <a name="ms-ds-user-password-not-required-attribute"></a>ms-DS-utente-password-attributo non obbligatorio

Indica se è necessaria una password per l'account a cui fa riferimento questo attributo. True se non è necessaria una password. in caso contrario, false.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-utente-password-non obbligatorio     |
| LDAP-Display-Name | ms-DS-UserPasswordNotRequired        |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1854              |
| System-ID-GUID    | 8f066172-a25e-4f53-8dcd-0a67d5fb883d |
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

In ADAM questo attributo sostituisce il flag [**Ads \_ UF \_ passwd \_ NOTREQD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl**](a-useraccountcontrol.md) .

 

