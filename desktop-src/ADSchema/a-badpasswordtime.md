---
title: Attributo Bad-Password-Time
description: Data e ora dell'ultimo tentativo di accesso a questo account con una password non valida.
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Bad-Password-Time
- Schema AD dell'attributo badPasswordTime
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2130e9bf09b70ee96c934027dc8369b8fdb73139396bc1aa1f9f7edffb4d7b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022769"
---
# <a name="bad-password-time-attribute"></a>Attributo Bad-Password-Time

Data e ora dell'ultimo tentativo di accesso a questo account con una password non valida. Questo valore viene archiviato come numero intero grande che rappresenta il numero di intervalli di 100 nanosecondi dal 1° gennaio 1601 (UTC). Il valore zero indica che l'ultima volta che è stata usata una password non corretta è sconosciuta.



| Voce | Valore |
|-------------------|-------------------------------------------|
| CN                | Ora password non valida                         |
| Ldap-Display-Name | badPasswordTime                           |
| Dimensione              | 8 byte                                   |
| Privilegio di aggiornamento  | Questo valore viene impostato dal sistema.          |
| Frequenza di aggiornamento  | Ogni volta che l'utente immette una password non valida. |
| Attribute-Id      | 1.2.840.113556.1.4.49                     |
| System-Id-Guid    | bf96792d-0de6-11d0-a285-00aa003049e2      |
| Sintassi            | [**Intervallo**](s-interval.md)            |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
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
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



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
| System-Flags           | 0x00000011                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|-------------------------------------------------------------------|
| ID collegamento                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Vero                                                              |
| Is-Single-Valued       | Vero                                                              |
| Indicizzato             | Falso                                                             |
| Nel catalogo globale      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000011                                                        |
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
| System-Flags           | 0x00000011                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



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
| System-Flags           | 0x00000011                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



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
| System-Flags           | 0x00000011                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



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
| System-Flags           | 0x00000011                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="remarks"></a>Commenti

La parte alta di questo intero di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte inferiore corrisponde al membro **dwLowDateTime** della struttura **FILETIME.**

Questo attributo non viene replicato e viene gestito separatamente in ogni controller di dominio nel dominio. Per ottenere un valore accurato per l'ora dell'ultima password non valida dell'utente nel dominio, è necessario eseguire query su ogni controller di dominio nel dominio. Il valore più grande ottenuto rappresenta l'ora vera e propria della password non valida.

 

