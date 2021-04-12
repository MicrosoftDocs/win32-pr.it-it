---
title: Attributo other-well-known-Objects
description: Contiene un elenco di contenitori per GUID e nome distinto. Questo consente il recupero di un oggetto dopo lo spostamento usando solo il GUID e il nome di dominio. Ogni volta che l'oggetto viene spostato, il sistema aggiorna automaticamente il nome distinto.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- Altri attributi-well-known-Object-schema AD
- Schema AD dell'attributo otherWellKnownObjects archiviato nel
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480272"
---
# <a name="other-well-known-objects-attribute"></a>Attributo other-well-known-Objects

Contiene un elenco di contenitori per GUID e nome distinto. Questo consente il recupero di un oggetto dopo lo spostamento usando solo il GUID e il nome di dominio. Ogni volta che l'oggetto viene spostato, il sistema aggiorna automaticamente il nome distinto.



| Voce | Valore |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Altri oggetti-well-known                                                                                                                                                                                      |
| LDAP-Display-Name | otherWellKnownObjects archiviato nel                                                                                                                                                                                         |
| Dimensione              | Esempio per il recupero del contenitore degli utenti nel dominio Microsoft: LDAP://(WKGUID = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com). Nota: le parentesi angolari sono sostituite da parentesi per evitare conflitti XML. |
| Privilegio aggiornamento  | Amministratore schema                                                                                                                                                                                          |
| Frequenza di aggiornamento  | Ogni volta che l'oggetto viene spostato.                                                                                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1359                                                                                                                                                                                       |
| System-ID-GUID    | 1ea64e5d-ac0f-11d2-90df-00c04fd91ab1                                                                                                                                                                          |
| Sintassi            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                               |



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
| System-Only            | Falso                           |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Falso                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



 

 





