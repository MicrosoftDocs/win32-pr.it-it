---
title: Attributo Canonical-Name
description: Nome dell'oggetto in formato canonico.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Schema AD Canonical-Name attribute
- attributo CanonicalName-schema AD
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875809"
---
# <a name="canonical-name-attribute"></a>Attributo Canonical-Name

Nome dell'oggetto in formato canonico. myserver2.fabrikam.com/users/jeffsmith è un esempio di nome distinto in formato canonico. Si tratta di un attributo costruito. I risultati restituiti sono identici a quelli restituiti dalla seguente funzione Active Directory: DsCrackNames (NULL, DS \_ Name \_ flag \_ sintattical \_ ONLY, DS \_ FQDN \_ 1779 \_ nome, \_ DS \_ nome canonico,...).

Per ulteriori informazioni sui formati dei nomi, vedere [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Canonical-Name                              |
| LDAP-Display-Name | canonicalName                               |
| Dimensione              | \-                                          |
| Privilegio aggiornamento  | \-                                          |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.916                      |
| System-ID-GUID    | 9a7ad945-ca53-11d1-bbd0-0080c76670c0        |
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
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



 

