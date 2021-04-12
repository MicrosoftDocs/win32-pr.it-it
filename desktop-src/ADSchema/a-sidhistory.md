---
title: Attributo SID-History
description: Contiene i SID precedenti utilizzati per l'oggetto se l'oggetto è stato spostato da un altro dominio.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Schema AD SID-History attribute
- Schema AD dell'attributo sIDHistory
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479921"
---
# <a name="sid-history-attribute"></a>Attributo SID-History

Contiene i SID precedenti utilizzati per l'oggetto se l'oggetto è stato spostato da un altro dominio. Ogni volta che un oggetto viene spostato da un dominio a un altro, viene creato un nuovo SID e il nuovo SID diventa objectSID. Il SID precedente viene aggiunto alla proprietà sIDHistory.



| Voce | Valore |
|-------------------|------------------------------------------------|
| CN                | SID-History                                    |
| LDAP-Display-Name | sIDHistory                                     |
| Dimensione              | \-                                             |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.               |
| Frequenza di aggiornamento  | Ogni volta che l'oggetto viene spostato in un nuovo dominio. |
| Attribute-Id      | 1.2.840.113556.1.4.609                         |
| System-ID-GUID    | 17eb4278-d167-11d0-b002-0000f80367c1           |
| Sintassi            | [**Stringa (SID)**](s-string-sid.md)            |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Vero                                                         |
| È a valore singolo       | Falso                                                        |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Falso                                                        |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Falso                                                        |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Falso                                                        |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Falso                                                        |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Falso                                                        |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



 

 





