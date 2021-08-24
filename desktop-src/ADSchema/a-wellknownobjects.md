---
title: Attributo Well-Known-Objects
description: Questo attributo contiene un elenco di contenitori di oggetti noti in base al GUID e al nome distinto.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Well-Known-Objects
- Schema AD dell'attributo wellKnownObjects
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5417b35ef821b1d84377c39eb4408eea57cf0dcc901ae0728a50ba48b88d6779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702411"
---
# <a name="well-known-objects-attribute"></a>Attributo Well-Known-Objects

Questo attributo contiene un elenco di contenitori di oggetti noti in base al GUID e al nome distinto. Gli oggetti noti sono contenitori di sistema. Queste informazioni vengono usate per recuperare un oggetto dopo che è stato spostato usando solo il GUID e il nome di dominio. Ogni volta che l'oggetto viene spostato, il sistema aggiorna automaticamente la parte del nome distinto dei valori Well-Known-Objects che fa riferimento all'oggetto. Il file Ntdsapi.h contiene le definizioni seguenti, che possono essere usate per recuperare un oggetto (i GUID associati a questi oggetti sono contenuti in Ntdsapi.h):

-   CONTENITORE \_ UTENTI \_ GUID \_ W
-   CONTENITORE \_ GUID COMPUTRS \_ \_ W
-   CONTENITORE \_ DEI SISTEMI GUID \_ \_ W
-   CONTENITORE \_ CONTROLLER DI DOMINIO GUID \_ \_ \_ W
-   CONTENITORE \_ \_ DELL'INFRASTRUTTURA \_ GUID W
-   CONTENITORE \_ OGGETTI GUID \_ ELIMINATI \_ \_ W
-   GUID \_ LOSTANDFOUND \_ CONTAINER \_ W
-   GUID \_ FOREIGNSECURITYPRINCIPALS \_ CONTAINER \_ W
-   CONTENITORE \_ DI DATI DEL PROGRAMMA GUID \_ \_ \_ W
-   GUID \_ MICROSOFT \_ PROGRAM \_ DATA \_ CONTAINER \_ W
-   GUID \_ NTDS \_ QUOTAS \_ CONTAINER \_ W



| Voce | Valore |
|-------------------|-------------------------------------------------|
| CN                | Oggetti noti                              |
| Ldap-Display-Name | wellKnownObjects                                |
| Dimensione              | \-                                              |
| Privilegio di aggiornamento  | Questo valore viene impostato dal sistema.                |
| Frequenza di aggiornamento  | Ogni volta che viene spostato uno dei contenitori di sistema. |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| System-Id-Guid    | 05308983-7688-11d1-aded-00c04fd8d5cd            |
| Sintassi            | [**Object(DN-Binary)**](s-object-dn-binary.md) |



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
| Is-Single-Valued       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



 

 





