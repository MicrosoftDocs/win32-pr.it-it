---
title: Attributo Dns-Root
description: Nome di dominio DNS più alto assegnato a una partizione di dominio/directory.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Schema AD Dns-Root attribute
- Schema AD dell'attributo dnsRoot
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303038"
---
# <a name="dns-root-attribute"></a>Attributo Dns-Root

Nome di dominio DNS più alto assegnato a una partizione di dominio/directory. Viene impostato su un oggetto crossRef e, tra le altre cose, viene usato per la generazione di riferimenti. Quando si esegue la ricerca in un intero albero di dominio, è necessario avviare la ricerca in corrispondenza dell'oggetto Dns-Root. Questo attributo può essere multivalore, nel qual caso vengono generati più riferimenti.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| LDAP-Display-Name | dnsRoot                                     |
| Dimensione              | \-                                          |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.            |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-ID-GUID    | bf967959-0de6-11d0-a285-00aa003049e2        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| È a valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi utilizzate in        | [**Riferimento incrociato**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| È a valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi utilizzate in        | [**Riferimento incrociato**](c-crossref.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| È a valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi utilizzate in        | [**Riferimento incrociato**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| È a valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi utilizzate in        | [**Riferimento incrociato**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| È a valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi utilizzate in        | [**Riferimento incrociato**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| È a valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi utilizzate in        | [**Riferimento incrociato**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| È a valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi utilizzate in        | [**Riferimento incrociato**](c-crossref.md)<br/> |



 

 





