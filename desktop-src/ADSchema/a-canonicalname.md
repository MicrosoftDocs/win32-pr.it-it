---
title: Canonical-Name attributo
description: Nome dell'oggetto in formato canonico.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Canonical-Name schema AD dell'attributo
- Schema AD dell'attributo canonicalName
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d88b31dd351e255c252188388bd1ba06b3a1c073163f5cd2cc9d2deac16a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307191"
---
# <a name="canonical-name-attribute"></a>Canonical-Name attributo

Nome dell'oggetto in formato canonico. myserver2.fabrikam.com/users/jeffsmith è un esempio di nome distinto in formato canonico. Si tratta di un attributo costruito. I risultati restituiti sono identici a quelli restituiti dalla funzione di Active Directory seguente: DsCrackNames(NULL, DS \_ NAME \_ FLAG \_ SYNTACTICAL \_ ONLY, DS \_ FQDN \_ 1779 \_ NAME, DS \_ CANONICAL \_ NAME, ...).

Per altre informazioni sui formati dei nomi, [**vedere DsCrackNames.**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa)



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Canonical-Name                              |
| Ldap-Display-Name | canonicalName                               |
| Dimensione              | \-                                          |
| Aggiorna privilegio  | \-                                          |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.916                      |
| System-Id-Guid    | 9a7ad945-ca53-11d1-bbd0-0080c76670c0        |
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
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



 

