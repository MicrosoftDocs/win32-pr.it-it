---
title: attributi ms-DS-has-instantied-NCs
description: Informazioni sullo stato di replica di DS, analoghe a (e un superset di) degli attributi hasMasterNCs e hasPartialReplicaNCs esistenti. Utilizzato da KCC durante la configurazione dei partner di replica.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di MS-DS-has-instantid-NCs
- attributo msDS-HasInstantiatedNCs-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480096"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>attributi ms-DS-has-instantied-NCs

Informazioni sullo stato di replica di DS, analoghe a (e un superset di) degli attributi hasMasterNCs e hasPartialReplicaNCs esistenti. Utilizzato da KCC durante la configurazione dei partner di replica.



| Voce | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-ha-creata un'istanza-NCs                                                                                                                                                                                  |
| LDAP-Display-Name | msDS-HasInstantiatedNCs                                                                                                                                                                                     |
| Dimensione              | 4 byte                                                                                                                                                                                                     |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.                                                                                                                                                                            |
| Frequenza di aggiornamento  | Circa due volte più spesso di hasMasterNCs/hasPartialReplicaNCs. Questi attributi esistenti vengono aggiornati solo quando il controller di dominio aggiunge o rimuove una partizione, ad esempio in caso di passaggio da un controller di dominio a un GC o viceversa. |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| System-ID-GUID    | 11e9a5bc-4517-4049-af9c-51554fb0fc09                                                                                                                                                                        |
| Sintassi            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
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
| È a valore singolo       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi utilizzate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| È a valore singolo       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi utilizzate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| È a valore singolo       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi utilizzate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| È a valore singolo       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi utilizzate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| È a valore singolo       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi utilizzate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vero                                     |
| È a valore singolo       | Falso                                    |
| Indicizzato             | Falso                                    |
| Nel catalogo globale      | Falso                                    |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classi utilizzate in        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





