---
title: Attributo Title
description: Contiene la posizione dell'utente. Questa proprietà viene comunemente usata per indicare la posizione formale, ad esempio Programmatore senior, anziché una classe di classe, ad esempio programmatore. Non viene in genere usato per i titoli dei suffissi, ad esempio Esq. o DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Title
- Title attribute AD Schema
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8885a557e8fbec17d6d58d68fdea0f99039f0e09e34a8da01954dc7b4979fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645031"
---
# <a name="title-attribute-ad-schema"></a>Attributo Title (schema AD)

Contiene la posizione dell'utente. Questa proprietà viene comunemente usata per indicare la posizione formale, ad esempio Programmatore senior, anziché una classe di classe, ad esempio programmatore. Non viene in genere usato per i titoli dei suffissi, ad esempio Esq. o DDS.



| Voce | Valore |
|-------------------|---------------------------------------------------------------------------|
| CN                | Titolo                                                                     |
| Ldap-Display-Name | title                                                                     |
| Dimensione              | \-                                                                        |
| Aggiorna privilegio  | Amministratore di dominio o proprietario dell'account.                                    |
| Frequenza di aggiornamento  | Quando viene creato il record dell'utente e ogni volta che è necessario modificare il titolo. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-Id-Guid    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Is-Single-Valued       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi usate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Is-Single-Valued       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi usate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Is-Single-Valued       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi usate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Is-Single-Valued       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi usate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Is-Single-Valued       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi usate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Is-Single-Valued       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi usate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



 

 





