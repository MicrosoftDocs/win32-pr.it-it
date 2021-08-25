---
title: Object-Classes attributo
description: Proprietà a più valori che contiene stringhe che rappresentano ogni classe nello schema. Ogni valore contiene governsID, lDAPDisplayName, mustContain, mayContain e così via.
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- Object-Classes schema AD dell'attributo
- Schema AD dell'attributo objectClasses
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c20c11ff547c24b37edab7f88a2854c9bc26ff133e7acba3a381971ededc3d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925191"
---
# <a name="object-classes-attribute"></a>Object-Classes attributo

Proprietà a più valori che contiene stringhe che rappresentano ogni classe nello schema. Ogni valore contiene governsID, lDAPDisplayName, mustContain, mayContain e così via.



| Voce | Valore |
|-------------------|--------------------------------------------------|
| CN                | Object-Classes                                   |
| Ldap-Display-Name | objectClasses                                    |
| Dimensione              | Circa 20 byte in media per ogni nome di classe.        |
| Privilegio di aggiornamento  | La finestra di progettazione dell'oggetto imposta questo valore. |
| Frequenza di aggiornamento  | Ogni volta che la progettazione della classe cambia.        |
| Attribute-Id      | 2.5.21.6                                         |
| System-Id-Guid    | 9a7ad94b-ca53-11d1-bbd0-0080c76670c0             |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)      |



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
|------------------------|---------------------------------------------|
| ID collegamento                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Vero                                        |
| Is-Single-Valued       | Falso                                       |
| Indicizzato             | Falso                                       |
| Nel catalogo globale      | Falso                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| Classi usate in        | [**SubSchema**](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------------------|
| ID collegamento                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Vero                                        |
| Is-Single-Valued       | Falso                                       |
| Indicizzato             | Falso                                       |
| Nel catalogo globale      | Falso                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| Classi usate in        | [**SubSchema**](c-subschema.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------------------|
| ID collegamento                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Vero                                        |
| Is-Single-Valued       | Falso                                       |
| Indicizzato             | Falso                                       |
| Nel catalogo globale      | Falso                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| Classi usate in        | [**Schema secondario**](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------------------|
| ID collegamento                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Vero                                        |
| A valore singolo       | Falso                                       |
| Indicizzato             | Falso                                       |
| Nel catalogo globale      | Falso                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| Classi usate in        | [**Schema secondario**](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------------------|
| ID collegamento                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Vero                                        |
| A valore singolo       | Falso                                       |
| Indicizzato             | Falso                                       |
| Nel catalogo globale      | Falso                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| Classi usate in        | [**Schema secondario**](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------------------|
| ID collegamento                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Vero                                        |
| A valore singolo       | Falso                                       |
| Indicizzato             | Falso                                       |
| Nel catalogo globale      | Falso                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| Classi usate in        | [**Schema secondario**](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------------------|
| ID collegamento                | \-                                          |
| MAPI-Id                | \-                                          |
| System-Only            | Vero                                        |
| A valore singolo       | Falso                                       |
| Indicizzato             | Falso                                       |
| Nel catalogo globale      | Falso                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                |
| Range-Lower            | \-                                          |
| Range-Upper            | \-                                          |
| Search-Flags           | 0x00000000                                  |
| System-Flags           | 0x08000014                                  |
| Classi usate in        | [**Schema secondario**](c-subschema.md)<br/> |



 

 





