---
title: Attributo title
description: Contiene il titolo del processo dell'utente. Questa proprietà viene comunemente usata per indicare il titolo formale del processo, ad esempio il programmatore Senior, invece della classe professionale, ad esempio il programmatore. Non viene in genere usato per i titoli dei suffissi, ad esempio la porta diesel. o DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Schema di AD attributo titolo
- Schema di AD attributo titolo
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbb4dae862db9fc363b22647bd5e56a98e9e60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875509"
---
# <a name="title-attribute-ad-schema"></a>Attributo title (schema AD)

Contiene il titolo del processo dell'utente. Questa proprietà viene comunemente usata per indicare il titolo formale del processo, ad esempio il programmatore Senior, invece della classe professionale, ad esempio il programmatore. Non viene in genere usato per i titoli dei suffissi, ad esempio la porta diesel. o DDS.



| Voce | Valore |
|-------------------|---------------------------------------------------------------------------|
| CN                | Titolo                                                                     |
| LDAP-Display-Name | title                                                                     |
| Dimensione              | \-                                                                        |
| Privilegio aggiornamento  | Amministratore di dominio o proprietario dell'account.                                    |
| Frequenza di aggiornamento  | Quando il record dell'utente viene creato e ogni volta che il titolo deve essere modificato. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-ID-GUID    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
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
| È a valore singolo       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| È a valore singolo       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| È a valore singolo       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| È a valore singolo       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| È a valore singolo       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| È a valore singolo       | Vero                                                                                                                            |
| Indicizzato             | Falso                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> |



 

 





