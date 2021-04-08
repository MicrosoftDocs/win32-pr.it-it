---
title: Attributo Trust-Attributes
description: Questo attributo archivia gli attributi di trust per un dominio trusted.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Schema AD Trust-Attributes attribute
- Schema AD dell'attributo trustAttributes
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744882"
---
# <a name="trust-attributes-attribute"></a>Attributo Trust-Attributes

Questo attributo archivia gli attributi di trust per un dominio trusted. I valori di attributo possibili sono i seguenti:

-   \_ \_ \_ Transitività non transitiva dell'attributo trust.
-   \_ \_ \_ L'attendibilità padre dell'albero degli attributi di attendibilità è impostata sul padre dell'albero dell'organizzazione.
-   Trust \_ \_ radice dell'albero degli attributi di attendibilità \_ impostato su un'altra radice dell'albero nell'insieme di strutture.
-   \_Attributo trust \_ di livello superiore \_ solo collegamento attendibile valido solo per client di livello superiore.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| LDAP-Display-Name | trustAttributes                      |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| System-ID-GUID    | 80a67e5a-9f22-11d0-afdd-00c04fd930c9 |
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
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Vero                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



 

 





