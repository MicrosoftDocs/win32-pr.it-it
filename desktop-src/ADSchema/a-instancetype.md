---
title: Attributo Instance-Type
description: Bit che determina il modo in cui viene creata un'istanza dell'oggetto in un determinato server.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Schema AD Instance-Type attribute
- Schema AD dell'attributo instanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744834"
---
# <a name="instance-type-attribute"></a>Attributo Instance-Type

Bit che determina il modo in cui viene creata un'istanza dell'oggetto in un determinato server. Il valore di questo attributo può variare in repliche diverse anche se le repliche sono sincronizzate.

Questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.

| Valore      | Descrizione                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | Intestazione del contesto dei nomi.                                                                        |
| 0x00000002 | Non è stata creata un'istanza della replica.                                                                  |
| 0x00000004 | L'oggetto è scrivibile in questa directory.                                                          |
| 0x00000008 | Viene mantenuto il contesto di denominazione sopra questo in questa directory.                                       |
| 0x00000010 | Il contesto dei nomi è in corso di costruzione per la prima volta tramite la replica. |
| 0x00000020 | Il contesto dei nomi è in corso di rimozione dal DSA locale.                          |



 



| Voce | Valore |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| LDAP-Display-Name | instanceType                                   |
| Dimensione              | 4 byte.                                       |
| Privilegio aggiornamento  | Questo valore viene impostato dall'amministratore dello schema. |
| Frequenza di aggiornamento  | Quando viene creato l'oggetto.                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| System-ID-GUID    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Sintassi            | [**Enumerazione**](s-enumeration.md)           |



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
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| È a valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| È a valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| È a valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| È a valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| È a valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| È a valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| È a valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



 

 





