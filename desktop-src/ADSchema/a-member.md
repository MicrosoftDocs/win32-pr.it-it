---
title: Attributo member
description: Elenco di utenti che appartengono al gruppo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo membro
- Attributo membro Schema DI ACTIVE Directory
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1efe13163946cb5be6ca83b5d0c7f964b8d6b1981ce45f79166af01bd62e6c9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705511"
---
# <a name="member-attribute"></a>Attributo member

Elenco di utenti che appartengono al gruppo.



| Voce | Valore |
|-------------------|-------------------------------------------------------|
| CN                | Membro                                                |
| Ldap-Display-Name | member                                                |
| Dimensione              | \-                                                    |
| Aggiorna privilegio  | Amministratore di dominio                                  |
| Frequenza di aggiornamento  | Ogni volta che un utente viene aggiunto o rimosso da un gruppo. |
| Attribute-Id      | 2.5.4.31                                              |
| System-Id-Guid    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Sintassi            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



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
|------------------------|-----------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | Falso                                                                                   |
| Is-Single-Valued       | Falso                                                                                   |
| Indicizzato             | Falso                                                                                   |
| Nel catalogo globale      | Vero                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Is-Single-Valued       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | Falso                               |
| Is-Single-Valued       | Falso                               |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Vero                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| Classi usate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Is-Single-Valued       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Is-Single-Valued       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Is-Single-Valued       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Is-Single-Valued       | Falso                                                                                                                                 |
| Indicizzato             | Falso                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Gruppo di nomi**](c-groupofnames.md)<br/> [**Gruppo MSMQ**](c-msmq-group.md)<br/> |



 

 





