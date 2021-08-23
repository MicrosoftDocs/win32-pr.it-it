---
title: Schema-Info attributo
description: Valore binario interno usato per rilevare le modifiche dello schema tra controller di dominio e forzare un ciclo di replica NC dello schema prima di replicare qualsiasi altro NC. Usato per risolvere i conflitti quando viene effettuato il seized dell'FSMO dello schema e viene apportata una modifica in più controller di dominio.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Schema-Info schema AD dell'attributo
- Schema AD dell'attributo schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa0d55dd29f207b84b0951ee448ba988d128fabfd126f38b2a4692d7cd3e0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646530"
---
# <a name="schema-info-attribute"></a>Schema-Info attributo

Valore binario interno usato per rilevare le modifiche dello schema tra controller di dominio e forzare un ciclo di replica NC dello schema prima di replicare qualsiasi altro NC. Usato per risolvere i conflitti quando viene effettuato il seized dell'FSMO dello schema e viene apportata una modifica in più controller di dominio.



| Voce | Valore |
|-------------------|-------------------------------------------------------|
| CN                | Schema-Info                                           |
| Ldap-Display-Name | schemaInfo                                            |
| Dimensione              | \-                                                    |
| Privilegio di aggiornamento  | Questo valore viene impostato dal sistema.                      |
| Frequenza di aggiornamento  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1358                               |
| System-Id-Guid    | f9fb64ae-93b4-11d2-9945-0000f87a57d4                  |
| Sintassi            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
| Nel catalogo globale      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**Dmd**](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



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
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**Dmd**](c-dmd.md)<br/> |



## <a name="adam"></a>Adam



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
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**Dmd**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**Dmd**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**Dmd**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**Dmd**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**Dmd**](c-dmd.md)<br/> |



 

 





