---
title: Attributo member
description: Elenco di utenti che appartengono al gruppo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo membro
- Schema di AD dell'attributo membro
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302983"
---
# <a name="member-attribute"></a>Attributo member

Elenco di utenti che appartengono al gruppo.



| Voce | Valore |
|-------------------|-------------------------------------------------------|
| CN                | Membro                                                |
| LDAP-Display-Name | member                                                |
| Dimensione              | \-                                                    |
| Privilegio aggiornamento  | Amministratore di dominio                                  |
| Frequenza di aggiornamento  | Ogni volta che un utente viene aggiunto o rimosso da un gruppo. |
| Attribute-Id      | 2.5.4.31                                              |
| System-ID-GUID    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Sintassi            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



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
|------------------------|-----------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | Falso                                                                                   |
| È a valore singolo       | Falso                                                                                   |
| Indicizzato             | Falso                                                                                   |
| Nel catalogo globale      | Vero                                                                                    |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| È a valore singolo       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | Falso                               |
| È a valore singolo       | Falso                               |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Vero                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| È a valore singolo       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| È a valore singolo       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| È a valore singolo       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| È a valore singolo       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



 

 





