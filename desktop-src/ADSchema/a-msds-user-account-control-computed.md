---
title: Attributo ms-DS-User-Account-Control-Computed
description: msDS-User-Account-Control-Computed è molto simile a userAccountControl, ma il valore dell'attributo può contenere bit aggiuntivi che non sono persistenti.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- Ms-DS-User-Account-Control-Computed attribute AD Schema
- Schema AD dell'attributo msDS-User-Account-Control-Computed
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8747bddccdfa65222072592b7f418fd35529d987f9903d71cddf5e01556fec53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763261"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>Attributo ms-DS-User-Account-Control-Computed

**msDS-User-Account-Control-Computed** è molto simile a [**userAccountControl,**](a-useraccountcontrol.md)ma il valore dell'attributo può contenere bit aggiuntivi che non sono persistenti. I bit calcolati includono quanto segue.



| Valore                | Nome (definito in Iads.h)                     |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **BLOCCO \_ UF**<br/>                   |
| 0x800000<br/>  | **PASSWORD UF \_ \_ SCADUTA**<br/>         |
| 0x4000000<br/> | **ACCOUNT DEI \_ SEGRETI \_ PARZIALI UF \_**<br/> |
| 0x8000000<br/> | **UF \_ USE \_ AES \_ KEYS**<br/>            |



 

L'elenco completo dei bit contenuti in [**User-Account-Control**](a-useraccountcontrol.md) e **pertanto msDS-User-Account-Control-Computed** è disponibile anche nella pagina di riferimento **User-Account-Control** (mappata tramite il flag [ADSI)](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) o nelle pagine di riferimento per la gestione della rete per la struttura user info [**\_ \_ 1008.**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008)



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Control-Computed  |
| Ldap-Display-Name | MsDS-User-Account-Control-Computed   |
| Dimensione              | \-                                   |
| Aggiorna privilegio  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| System-Id-Guid    | 2cc4b836-b63f-4940-8d23-ea7acf06af56 |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



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
| Classi usate in        | [**Ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| A valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| A valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| A valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



 

