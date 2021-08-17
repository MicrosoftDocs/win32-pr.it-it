---
title: Dns-Root attributo
description: Nome di dominio DNS in alto assegnato a una partizione di dominio/directory.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Dns-Root schema AD dell'attributo
- Attributo dnsRoot Schema di AD
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f87acecb86fcd8ca8af4bbc2917dbe5381deaf4e5722a5803d31f186e57e04d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961580"
---
# <a name="dns-root-attribute"></a>Dns-Root attributo

Nome di dominio DNS in alto assegnato a una partizione di dominio/directory. Questa proprietà viene impostata su un oggetto crossRef e viene usata, tra le altre cose, per la generazione di segnalazioni. Quando si esegue una ricerca in un intero albero di dominio, la ricerca deve essere avviata in corrispondenza dellDns-Root o object. Questo attributo può essere multivalore, nel qual caso vengono generate più segnalazioni.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| Ldap-Display-Name | dnsRoot                                     |
| Dimensione              | \-                                          |
| Aggiorna privilegio  | Questo valore viene impostato dal sistema.            |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-Id-Guid    | bf967959-0de6-11d0-a285-00aa003049e2        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Is-Single-Valued       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi usate in        | [**Riferimenti incrociati**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Is-Single-Valued       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi usate in        | [**Riferimenti incrociati**](c-crossref.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Is-Single-Valued       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi usate in        | [**Riferimenti incrociati**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| A valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi usate in        | [**Riferimenti incrociati**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| A valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi usate in        | [**Riferimenti incrociati**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| A valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi usate in        | [**Riferimenti incrociati**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------|
| ID collegamento                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| A valore singolo       | Falso                                      |
| Indicizzato             | Vero                                       |
| Nel catalogo globale      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classi usate in        | [**Riferimenti incrociati**](c-crossref.md)<br/> |



 

 





