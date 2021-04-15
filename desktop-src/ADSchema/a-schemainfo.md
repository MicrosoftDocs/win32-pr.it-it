---
title: Attributo Schema-Info
description: Valore binario interno utilizzato per rilevare le modifiche dello schema tra i controller di dominio e forzare un ciclo di replica NC dello schema prima di replicare qualsiasi altro NC. Utilizzato per risolvere i vincoli quando viene sequestrato l'FSMO dello schema e viene apportata una modifica a più di un controller di dominio.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Schema AD Schema-Info attribute
- Schema AD dell'attributo schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520022"
---
# <a name="schema-info-attribute"></a>Attributo Schema-Info

Valore binario interno utilizzato per rilevare le modifiche dello schema tra i controller di dominio e forzare un ciclo di replica NC dello schema prima di replicare qualsiasi altro NC. Utilizzato per risolvere i vincoli quando viene sequestrato l'FSMO dello schema e viene apportata una modifica a più di un controller di dominio.



| Voce | Valore |
|-------------------|-------------------------------------------------------|
| CN                | Schema-Info                                           |
| LDAP-Display-Name | schemaInfo                                            |
| Dimensione              | \-                                                    |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.                      |
| Frequenza di aggiornamento  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1358                               |
| System-ID-GUID    | f9fb64ae-93b4-11d2-9945-0000f87a57d4                  |
| Sintassi            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**DMD**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**DMD**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**DMD**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**DMD**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**DMD**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**DMD**](c-dmd.md)<br/> |



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
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**DMD**](c-dmd.md)<br/> |



 

 





