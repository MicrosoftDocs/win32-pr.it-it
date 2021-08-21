---
title: Attributo Repl-UpToDate-Vector
description: Tiene traccia delle informazioni sullo stato della replica interna per un intero NC. Le informazioni qui possono essere estratte in forma pubblica tramite l'API DsReplicaGetInfo(). Presente in tutti gli oggetti radice NC.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Repl-UpToDate-Vector
- Schema AD dell'attributo replUpToDateVector
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 413291da92f52e0e6241e6dcfb6ca50303ed5740d370b1f5f900904266a75446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423732"
---
# <a name="repl-uptodate-vector-attribute"></a>Attributo Repl-UpToDate-Vector

Tiene traccia delle informazioni sullo stato della replica interna per un intero NC. Le informazioni qui possono essere estratte in forma pubblica tramite l'API DsReplicaGetInfo(). Presente in tutti gli oggetti radice NC.



| Voce | Valore |
|-------------------|--------------------------------------------------------------------------------|
| CN                | Repl-UpToDate-Vector                                                           |
| Ldap-Display-Name | replUpToDateVector                                                             |
| Dimensione              | La lunghezza è proporzionale al numero di repliche (passate e presenti) del NC. |
| Aggiorna privilegio  | Questo valore viene impostato dal sistema.                                               |
| Frequenza di aggiornamento  | Modifiche in risposta ai cicli di replica in ingresso completati.                   |
| Attribute-Id      | 1.2.840.113556.1.4.4                                                           |
| System-Id-Guid    | bf967a16-0de6-11d0-a285-00aa003049e2                                           |
| Sintassi            | [**Object(Replica-Link)**](s-object-replica-link.md)                          |



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
| A valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| A valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vero                            |
| Is-Single-Valued       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



 

 





