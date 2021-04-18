---
title: Attributo Account-Expires
description: Data di scadenza dell'account.
ms.assetid: 8c3c565e-77fe-4e8b-970a-8396fc6b45aa
ms.tgt_platform: multiple
keywords:
- Schema AD Account-Expires attribute
- Schema AD dell'attributo accountExpires
topic_type:
- apiref
api_name:
- Account-Expires
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb5041c544f96f79ad4c3172d776ebe909b1983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303590"
---
# <a name="account-expires-attribute"></a>Attributo Account-Expires

Data di scadenza dell'account. Questo valore rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC). Il valore 0 o 0x7FFFFFFFFFFFFFFF (9223372036854775807) indica che l'account non scade mai.



| Voce | Valore |
|-------------------|------------------------------------------------------------------------|
| CN                | Account-Expires                                                        |
| LDAP-Display-Name | accountExpires                                                         |
| Dimensione              | 8 byte                                                                |
| Privilegio aggiornamento  | Questo attributo viene impostato dall'amministratore di dominio.                          |
| Frequenza di aggiornamento  | Ogni volta che la data di scadenza precedente scade e deve essere aggiornata. |
| Attribute-Id      | 1.2.840.113556.1.4.159                                                 |
| System-ID-GUID    | bf967915-0de6-11d0-a285-00aa003049e2                                   |
| Sintassi            | [**Interval**](s-interval.md)                                         |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



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
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



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
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
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
| Search-Flags           | 0x00000010                                                        |
| System-Flags           | 0x00000010                                                        |
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
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
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
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
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
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
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
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="remarks"></a>Commenti

La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** .

 

