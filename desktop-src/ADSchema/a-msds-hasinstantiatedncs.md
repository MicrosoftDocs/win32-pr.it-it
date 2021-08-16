---
title: Attributo ms-DS-Has-Instantiated-NCs
description: Le informazioni sullo stato della replica DS, analoghe a (e a un superset di) gli attributi esistenti hannoMasterNCs e hasPartialReplicaNCs. Da usare da KCC durante la configurazione dei partner di replica.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-Has-Instantiated-NCs
- Schema AD dell'attributo msDS-HasInstantiatedNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efde9ef1cd9a7230e4493d3e542e1f5f661ed33027ad3e9a88ded9679df812c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804052"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>Attributo ms-DS-Has-Instantiated-NCs

Le informazioni sullo stato della replica DS, analoghe a (e a un superset di) gli attributi esistenti hannoMasterNCs e hasPartialReplicaNCs. Da usare da KCC durante la configurazione dei partner di replica.



| Voce | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Has-Instantiated-NCs                                                                                                                                                                                  |
| Ldap-Display-Name | msDS-HasInstantiatedNCs                                                                                                                                                                                     |
| Dimensione              | 4 byte                                                                                                                                                                                                     |
| Privilegio di aggiornamento  | Questo valore viene impostato dal sistema.                                                                                                                                                                            |
| Frequenza di aggiornamento  | Circa il doppio della frequenza di hasMasterNCs/hasPartialReplicaNCs. Questi attributi esistenti vengono aggiornati solo quando il controller di dominio aggiunge o rimuove una partizione ,ad esempio quando si cambia da controller di dominio a GC o viceversa. |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| System-Id-Guid    | 11e9a5bc-4517-4049-af9c-51554fb0fc09                                                                                                                                                                        |
| Sintassi            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| Is-Single-Valued       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| Is-Single-Valued       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| Is-Single-Valued       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| Is-Single-Valued       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| Is-Single-Valued       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| Is-Single-Valued       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





