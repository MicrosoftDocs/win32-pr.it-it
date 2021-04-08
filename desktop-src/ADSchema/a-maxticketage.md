---
title: Attributo max-ticket-Age
description: Questo attributo determina la quantità massima di tempo, in ore, che un ticket di concessione ticket (TGT) di un utente può essere utilizzato per l'autenticazione Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo max-ticket-Age
- Schema AD dell'attributo maxTicketAge
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744346"
---
# <a name="max-ticket-age-attribute"></a>Attributo max-ticket-Age

Questo attributo determina la quantità massima di tempo, in ore, che un ticket di concessione ticket (TGT) di un utente può essere utilizzato per l'autenticazione Kerberos. Quando il TGT di un utente scade, ne deve essere richiesto uno nuovo oppure è necessario rinnovarne uno esistente. Per impostazione predefinita, questa impostazione è impostata su 10 ore nell'oggetto Criteri di gruppo dominio predefinito (GPO).



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Numero massimo-ticket-Age                       |
| LDAP-Display-Name | maxTicketAge                         |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-ID-GUID    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Sintassi            | [**Interval**](s-interval.md)       |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| È a valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| È a valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| È a valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| È a valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| È a valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| È a valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



 

 





