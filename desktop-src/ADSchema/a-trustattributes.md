---
title: Trust-Attributes attributo
description: Questo attributo archivia gli attributi di trust per un dominio trusted.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Trust-Attributes schema AD dell'attributo
- Schema AD dell'attributo trustAttributes
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d09104d0f32c770ba1fe3fbdde6cf56d56989a801856ba970284b2d06c96a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704041"
---
# <a name="trust-attributes-attribute"></a>Trust-Attributes attributo

Questo attributo archivia gli attributi di trust per un dominio trusted. I valori possibili dell'attributo sono i seguenti:

-   TRUST \_ ATTRIBUTE \_ NON \_ TRANSITIVE Disabilita la transitività.
-   TRUST \_ ATTRIBUTE TREE PARENT Trust è impostato \_ \_ sull'elemento padre dell'albero dell'organizzazione.
-   TRUST \_ ATTRIBUTE TREE ROOT Trust impostato su \_ \_ un'altra radice dell'albero nella foresta.
-   TRUST \_ ATTRIBUTE \_ UPLEVEL ONLY Collegamento \_ attendibile valido solo per il client di livello superiore.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| Ldap-Display-Name | trustAttributes                      |
| Dimensione              | \-                                   |
| Privilegio di aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| System-Id-Guid    | 80a67e5a-9f22-11d0-afdd-00c04fd930c9 |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



 

 





