---
title: Admin-Count attributo
description: Indica che gli ACL di un determinato oggetto sono stati modificati in un valore più sicuro dal sistema perché era membro di uno dei gruppi amministrativi (direttamente o in modo transitivo).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Admin-Count schema AD dell'attributo
- Schema AD dell'attributo adminCount
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d652d53627643e1028ee73cc67678119c689e46d8f4ec289c92ca32127e098dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022849"
---
# <a name="admin-count-attribute"></a>Admin-Count attributo

Indica che gli ACL di un determinato oggetto sono stati modificati in un valore più sicuro dal sistema perché era membro di uno dei gruppi amministrativi (direttamente o in modo transitivo).



| Voce | Valore |
|-------------------|-----------------------------------------------------|
| CN                | Admin-Count                                         |
| Ldap-Display-Name | adminCount                                          |
| Dimensione              | 4 byte                                             |
| Privilegio di aggiornamento  | Questo valore viene impostato dal sistema.                    |
| Frequenza di aggiornamento  | Quando un oggetto viene aggiunto a un gruppo amministrativo. |
| Attribute-Id      | 1.2.840.113556.1.4.150                              |
| System-Id-Guid    | bf967918-0de6-11d0-a285-00aa003049e2                |
| Sintassi            | [**Enumerazione**](s-enumeration.md)                |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------|
| ID collegamento                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Is-Single-Valued       | Vero                                                                  |
| Indicizzato             | Falso                                                                 |
| Nel catalogo globale      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------|
| ID collegamento                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Is-Single-Valued       | Vero                                                                  |
| Indicizzato             | Falso                                                                 |
| Nel catalogo globale      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------|
| ID collegamento                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Is-Single-Valued       | Vero                                                                  |
| Indicizzato             | Falso                                                                 |
| Nel catalogo globale      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------|
| ID collegamento                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Is-Single-Valued       | Vero                                                                  |
| Indicizzato             | Falso                                                                 |
| Nel catalogo globale      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------|
| ID collegamento                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Is-Single-Valued       | Vero                                                                  |
| Indicizzato             | Falso                                                                 |
| Nel catalogo globale      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------|
| ID collegamento                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Is-Single-Valued       | Vero                                                                  |
| Indicizzato             | Falso                                                                 |
| Nel catalogo globale      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classi usate in        | [**Group**](c-group.md)<br/> [**Utente**](c-user.md)<br/> |



 

 





