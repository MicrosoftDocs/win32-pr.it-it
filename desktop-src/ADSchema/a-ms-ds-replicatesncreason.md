---
title: Attributo MS-DS-Replicates-NC-Reason
description: Attributo dell'oggetto ntdsConnection che indica il motivo (o se) KCC indica che la connessione è utile nella topologia di replica. È a più valori e ha la sintassi DistName+Binary, in cui la parte binaria è un campo di bit di dimensioni int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-DS-Replicates-NC-Reason
- Schema AD dell'attributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681105fe24584afae275a8869ad04698ff7a70daa32832140a98865318672863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118686972"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>Attributo MS-DS-Replicates-NC-Reason

Attributo dell'oggetto ntdsConnection che indica il motivo (o se) KCC indica che la connessione è utile nella topologia di replica. È a più valori e ha la sintassi DistName+Binary, in cui la parte binaria è un campo di bit di dimensioni int.



| Voce | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Ms-DS-Replicates-NC-Reason                                                                                                                 |
| Ldap-Display-Name | mS-DS-ReplicatesNCReason                                                                                                                   |
| Dimensione              | Valore per la parte binaria: 0 = NO \_ REASON,1 = TOPOLOGIA \_ GC, 2 = TOPOLOGIA \_ RING, 4 = MINIMIZE \_ HOPS \_ TOPOLOGY, 8 = TOPOLOGIA \_ \_ SERVER NON AGGIORNATA. |
| Privilegio di aggiornamento  | Questo valore viene impostato dal sistema.                                                                                                           |
| Frequenza di aggiornamento  | Può cambiare in risposta alle modifiche nella topologia di rete.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-Id-Guid    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Sintassi            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



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
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| Is-Single-Valued       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi usate in        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| Is-Single-Valued       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi usate in        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| Is-Single-Valued       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi usate in        | [**Connessione NTDS**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| A valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi usate in        | [**Connessione NTDS**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| A valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi usate in        | [**Connessione NTDS**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| A valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi usate in        | [**Connessione NTDS**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------------|
| ID collegamento                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| A valore singolo       | Falso                                                  |
| Indicizzato             | Falso                                                  |
| Nel catalogo globale      | Falso                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classi usate in        | [**Connessione NTDS**](c-ntdsconnection.md)<br/> |



 

 





