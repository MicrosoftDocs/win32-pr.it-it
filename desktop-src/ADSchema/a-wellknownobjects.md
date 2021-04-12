---
title: Attributo well-known-Objects
description: Questo attributo contiene un elenco di contenitori di oggetti noti per GUID e nome distinto.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo well-known-Objects
- Schema AD dell'attributo wellKnownObjects
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480200"
---
# <a name="well-known-objects-attribute"></a>Attributo well-known-Objects

Questo attributo contiene un elenco di contenitori di oggetti noti per GUID e nome distinto. Gli oggetti noti sono contenitori di sistema. Queste informazioni vengono utilizzate per recuperare un oggetto dopo che è stato spostato utilizzando solo il GUID e il nome di dominio. Ogni volta che l'oggetto viene spostato, il sistema aggiorna automaticamente la parte del nome distinto dei valori degli oggetti noti che fanno riferimento all'oggetto. Il file ntdsapi. h contiene le seguenti definizioni, che possono essere usate per recuperare un oggetto (i GUID associati a questi oggetti sono contenuti in ntdsapi. h):

-   \_contenitore utenti \_ GUID \_ W
-   \_contenitore di calcolo \_ GUID \_ W
-   \_contenitore di sistemi GUID \_ \_ W
-   \_contenitore controller di dominio GUID \_ \_ \_ W
-   \_contenitore infrastruttura \_ GUID \_ W
-   \_ \_ contenitore oggetti eliminati \_ GUID \_ W
-   GUID \_ LOSTANDFOUND \_ contenitore \_ W
-   GUID \_ FOREIGNSECURITYPRINCIPALS \_ contenitore \_ W
-   \_contenitore di dati del programma GUID \_ \_ \_ W
-   \_contenitore di \_ dati del programma Microsoft GUID \_ \_ \_ W
-   \_ \_ contenitore quote NTDS GUID \_ \_ W



| Voce | Valore |
|-------------------|-------------------------------------------------|
| CN                | Oggetti noti                              |
| LDAP-Display-Name | wellKnownObjects                                |
| Dimensione              | \-                                              |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.                |
| Frequenza di aggiornamento  | Ogni volta che uno dei contenitori di sistema viene spostato. |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| System-ID-GUID    | 05308983-7688-11d1-aded-00c04fd8d5cd            |
| Sintassi            | [**Object(DN-Binary)**](s-object-dn-binary.md) |



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
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



 

 





