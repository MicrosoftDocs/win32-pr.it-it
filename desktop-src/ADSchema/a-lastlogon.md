---
title: Attributo Last-Logon
description: Ultima volta in cui l'utente ha effettuato l'accesso.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Schema AD Last-Logon attribute
- Schema AD dell'attributo lastLogon
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875462"
---
# <a name="last-logon-attribute"></a>Attributo Last-Logon

Ultima volta in cui l'utente ha effettuato l'accesso. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC). Un valore pari a zero indica che l'ora dell'ultimo accesso è sconosciuta.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Last-Logon                           |
| LDAP-Display-Name | lastLogon                            |
| Dimensione              | 8 byte                              |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.     |
| Frequenza di aggiornamento  | Ogni volta che l'utente esegue l'accesso.          |
| Attribute-Id      | 1.2.840.113556.1.4.52                |
| System-ID-GUID    | bf967997-0de6-11d0-a285-00aa003049e2 |
| Sintassi            | [**Interval**](s-interval.md)       |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="remarks"></a>Commenti

La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** .

Questo attributo non viene replicato e viene mantenuto separatamente in ogni controller di dominio nel dominio. Per ottenere un valore accurato per l'ultimo accesso dell'utente nel dominio, è necessario recuperare l'attributo **Last-Logon** per l'utente da ogni controller di dominio nel dominio. Il valore più grande recuperato è l'ora dell'ultimo accesso true per tale utente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

