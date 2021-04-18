---
title: Attributo Lockout-Time
description: Data e ora (UTC) in cui l'account è stato bloccato.
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- Schema AD Lockout-Time attribute
- Schema AD dell'attributo lockoutTime
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303315"
---
# <a name="lockout-time-attribute"></a>Attributo Lockout-Time

Data e ora (UTC) in cui l'account è stato bloccato. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC). Un valore pari a zero indica che l'account non è attualmente bloccato.



| Voce | Valore |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Lockout-Time                                                                     |
| LDAP-Display-Name | lockoutTime                                                                      |
| Dimensione              | 8 byte                                                                          |
| Privilegio aggiornamento  | Amministratore di dominio                                                             |
| Frequenza di aggiornamento  | Quando il record dell'utente viene creato e ogni volta che è necessario modificare il tempo di blocco. |
| Attribute-Id      | 1.2.840.113556.1.4.662                                                           |
| System-ID-GUID    | 28630ebf-41d5-11d1-a9c1-0000f80367c1                                             |
| Sintassi            | [**Interval**](s-interval.md)                                                   |



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
| Search-Flags           | 0x00000000                        |
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
| Search-Flags           | 0x00000000                        |
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
| Search-Flags           | 0x00000000                                                        |
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
| Search-Flags           | 0x00000000                        |
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
| Search-Flags           | 0x00000000                        |
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
| Search-Flags           | 0x00000000                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="remarks"></a>Commenti

La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** .

Il valore di questo attributo viene reimpostato solo quando l'account viene registrato correttamente. Questo significa che questo valore può essere diverso da zero, ma l'account non è bloccato. Per determinare in modo accurato se l'account è bloccato, è necessario aggiungere la [**durata del blocco**](a-lockoutduration.md) a questa ora e confrontare il risultato con l'ora corrente, considerando i fusi orari locali e l'ora legale.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**Blocco-durata**](a-lockoutduration.md)
</dt> </dl>

 

