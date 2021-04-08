---
title: attributo di tipo DHCP
description: Tipo di server DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di tipo DHCP
- Schema AD dell'attributo dhcpType
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965103"
---
# <a name="dhcp-type-attribute"></a>attributo di tipo DHCP

Tipo di server DHCP. Questo attributo è impostato su tutti gli oggetti di objectClass [**dHCPClass**](c-dhcpclass.md). Il valore definisce il tipo di oggetto:

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| Voce | Valore |
|-------------------|--------------------------------------------------------|
| CN                | Tipo DHCP                                              |
| LDAP-Display-Name | dhcpType                                               |
| Dimensione              | 4 byte                                                |
| Privilegio aggiornamento  | Amministratore di dominio.                                  |
| Frequenza di aggiornamento  | Quando un nuovo server viene aggiunto o rimosso dalla foresta. |
| Attribute-Id      | 1.2.840.113556.1.4.699                                 |
| System-ID-GUID    | 963d273b-48be-11d1-a9c3-0000f80367c1                   |
| Sintassi            | [**Enumerazione**](s-enumeration.md)                   |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| È a valore singolo       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi utilizzate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| È a valore singolo       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi utilizzate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| È a valore singolo       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi utilizzate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| È a valore singolo       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi utilizzate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| È a valore singolo       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi utilizzate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| È a valore singolo       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi utilizzate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



 

 





