---
title: Attributo dhcp-Type
description: Tipo di server DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo dhcp-Type
- Schema AD dell'attributo dhcpType
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f4cc64a05db9b88d13a1e7dfb3ce0976391b9d2514388ae9045eb11d97a5b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049651"
---
# <a name="dhcp-type-attribute"></a>Attributo dhcp-Type

Tipo di server DHCP. Questo attributo è impostato su tutti gli oggetti di objectClass [**dHCPClass**](c-dhcpclass.md). Il relativo valore definisce il tipo di oggetto:

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| Voce | Valore |
|-------------------|--------------------------------------------------------|
| CN                | dhcp-Type                                              |
| Ldap-Display-Name | dhcpType                                               |
| Dimensione              | 4 byte                                                |
| Privilegio di aggiornamento  | Amministratore di dominio.                                  |
| Frequenza di aggiornamento  | Quando viene aggiunto o rimosso un nuovo server dalla foresta. |
| Attribute-Id      | 1.2.840.113556.1.4.699                                 |
| System-Id-Guid    | 963d273b-48be-11d1-a9c3-0000f80367c1                   |
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
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Vero                                         |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



 

 





