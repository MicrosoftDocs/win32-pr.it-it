---
title: Attributo UAS-Compat
description: Indica se il gestore degli account di sicurezza imporrà le dimensioni dei dati per rendere Active Directory compatibile con LanManager user account System (UAS).
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Schema AD UAS-Compat attribute
- Schema AD dell'attributo uASCompat
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303352"
---
# <a name="uas-compat-attribute"></a>Attributo UAS-Compat

Indica se il gestore degli account di sicurezza imporrà le dimensioni dei dati per rendere Active Directory compatibile con LanManager user account System (UAS). Se questo valore è 0, non viene applicato alcun limite. Se questo valore è 1, vengono applicati i limiti seguenti.



| Valore                          | Length                         |
|--------------------------------|--------------------------------|
| Password<br/>            | da 0 a 14 caratteri<br/>  |
| Nome account<br/>        | da 0 a 20 caratteri<br/>  |
| Nome dominio<br/>         | da 0 a 15 caratteri<br/>  |
| Nome computer<br/>       | da 0 a 15 caratteri<br/>  |
| Commenti<br/>            | da 0 a 48 caratteri<br/>  |
| Home directory<br/>      | da 0 a 256 caratteri<br/> |
| Percorso script<br/>         | da 0 a 256 caratteri<br/> |
| Unità di tempo per settimana<br/> | 168 bit (21 byte)<br/> |



 



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| LDAP-Display-Name | uASCompat                            |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | Eseguita da un amministratore.       |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| System-ID-GUID    | bf967a61-0de6-11d0-a285-00aa003049e2 |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| È a valore singolo       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| È a valore singolo       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| È a valore singolo       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| È a valore singolo       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| È a valore singolo       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| È a valore singolo       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



 

 





