---
title: ms-DS-User-Account-Control-attributo calcolato
description: msDS-User-Account-Control-calcolato è molto simile a userAccountControl, ma il valore dell'attributo può contenere bit aggiuntivi che non sono salvati in modo permanente.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Account-Control-schema AD dell'attributo calcolato
- msDS-User-Account-Control-schema AD dell'attributo calcolato
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303235"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>ms-DS-User-Account-Control-attributo calcolato

**msDS-User-Account-Control-calcolato** è molto simile a [**userAccountControl**](a-useraccountcontrol.md), ma il valore dell'attributo può contenere bit aggiuntivi che non sono salvati in modo permanente. I bit calcolati includono quanto segue.



| Valore                | Nome (definito in IADs. h)                     |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **\_blocco UF**<br/>                   |
| 0x800000<br/>  | **\_password UF \_ scaduta**<br/>         |
| 0x4000000<br/> | **\_account dei \_ segreti PARZIALi UF \_**<br/> |
| 0x8000000<br/> | **UF \_ usare \_ \_ chiavi AES**<br/>            |



 

L'elenco completo dei bit che possono essere contenuti da [**User-Account-Control**](a-useraccountcontrol.md) e quindi da **msDS-User-Account-Control-Compute** è disponibile nella pagina di riferimento **User-Account-Control** (mappata tramite il flag [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) ) o nelle pagine di riferimento per la gestione della rete per la struttura [**\_ Info utente \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Control-calcolato  |
| LDAP-Display-Name | msDS-User-Account-Control-calcolato   |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| System-ID-GUID    | 2cc4b836-b63f-4940-8d23-ea7acf06af56 |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
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
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



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



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



 

