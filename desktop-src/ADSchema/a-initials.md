---
title: Attributo Initials
description: Contiene le iniziali per le parti del nome completo dell'utente. Può essere usato come iniziale intermedia nel Windows Rubrica.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Initials
- Attributo initials Schema di ACTIVE Directory
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c9aa6020dc5f442547582c71be475c7dc8e6e3efcd3e1588095c536f22e2347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322911"
---
# <a name="initials-attribute"></a>Attributo Initials

Contiene le iniziali per le parti del nome completo dell'utente. Può essere usato come iniziale intermedia nel Windows Rubrica.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Iniziali                                    |
| Ldap-Display-Name | Initials                                    |
| Dimensione              | \-                                          |
| Aggiorna privilegio  | Amministratore di dominio o proprietario dell'account.      |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 2.5.4.43                                    |
| System-Id-Guid    | f0f8ff90-1191-11d0-a060-00aa006c33ed        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|--------------------------------------------------------------------|
| ID collegamento                | \-                                                                 |
| MAPI-Id                | 0x3A0A                                                             |
| System-Only            | Falso                                                              |
| Is-Single-Valued       | Vero                                                               |
| Indicizzato             | Falso                                                              |
| Nel catalogo globale      | Falso                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 6                                                                  |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classi usate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Is-Single-Valued       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Is-Single-Valued       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| A valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| A valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| A valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





