---
title: MS-DS-replicates-NC-Reason (attributo)
description: Attributo dell'oggetto ntdsConnection che indica perché, o se il KCC Mostra che la connessione è utile nella topologia di replica. È a più valori e ha la sintassi binaria DistName +, dove la parte binaria è un bit di dimensioni int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- MS-DS-replicas-schema AD dell'attributo NC-Reason
- Schema AD dell'attributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104400964"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>MS-DS-replicates-NC-Reason (attributo)

Attributo dell'oggetto ntdsConnection che indica perché, o se il KCC Mostra che la connessione è utile nella topologia di replica. È a più valori e ha la sintassi binaria DistName +, dove la parte binaria è un bit di dimensioni int.



| Voce | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-replicas-NC-Reason                                                                                                                 |
| LDAP-Display-Name | mS-DS-ReplicatesNCReason                                                                                                                   |
| Dimensione              | Valore per la parte binaria: 0 = nessun \_ motivo, 1 = \_ topologia GC, 2 = \_ topologia ad anello, 4 = riduzione della \_ topologia degli hop \_ , 8 = \_ topologia di server non aggiornati \_ . |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.                                                                                                           |
| Frequenza di aggiornamento  | Può cambiare in risposta alle modifiche nella topologia di rete.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-ID-GUID    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Sintassi            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



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
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| È a valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi utilizzate in        | [**NTDS-connessione**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| È a valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi utilizzate in        | [**NTDS-connessione**](c-ntdsconnection.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| È a valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi utilizzate in        | [**NTDS-connessione**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| È a valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi utilizzate in        | [**NTDS-connessione**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| È a valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi utilizzate in        | [**NTDS-connessione**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| È a valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi utilizzate in        | [**NTDS-connessione**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| È a valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi utilizzate in        | [**NTDS-connessione**](c-ntdsconnection.md)<br/> |



 

 





