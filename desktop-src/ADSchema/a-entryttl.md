---
title: Entry-TTL (attributo)
description: Questo attributo operativo è gestito dal server e sembra essere presente in ogni voce dinamica.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Entry-TTL attributo AD schema
- Schema AD dell'attributo entryTTL
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479712"
---
# <a name="entry-ttl-attribute"></a>Entry-TTL (attributo)

Questo attributo operativo è gestito dal server e sembra essere presente in ogni voce dinamica. L'attributo non è presente se la voce non contiene la classe di oggetti dynamicObject. Il valore di questo attributo è il tempo, in secondi, in cui la voce continuerà a esistere prima di scomparire dalla directory. In assenza di operazioni "Refresh", i valori restituiti leggendo l'attributo in due ricerche successive sono garantiti che non aumentano. Il valore minimo consentito è 0, che indica che la voce può scomparire senza preavviso. L'attributo è contrassegnato come nessuna modifica da parte dell'utente perché può essere modificato solo tramite l'operazione di aggiornamento.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Voce-TTL                                   |
| LDAP-Display-Name | entryTTL                                    |
| Dimensione              | 4 byte. Massimo = 1 anno, valore predefinito = 1 giorno. |
| Privilegio aggiornamento  | \-                                          |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| System-ID-GUID    | d213decc-d81a-4384-AAC2-dcfcfd631cf8        |
| Sintassi            | [**Enumerazione**](s-enumeration.md)        |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi utilizzate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi utilizzate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi utilizzate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi utilizzate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi utilizzate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi utilizzate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



 

 





