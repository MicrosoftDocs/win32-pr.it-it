---
title: Attributo PARENT-GUID
description: Si tratta di un attributo costruito, che ha lo scopo di supportare il controllo DirSync. Questo attributo contiene l'objectGuid dell'elemento padre di un oggetto quando si replica la creazione, la ridenominazione o lo spostamento di un oggetto.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo PARENT-GUID
- Schema AD dell'attributo parentGUID
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f42ba5aedc73f04d8967b84bcfbff39c54ce0dbcdf769e48a747ffa0d3e8c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119325431"
---
# <a name="parent-guid-attribute"></a>Attributo PARENT-GUID

Si tratta di un attributo costruito, che ha lo scopo di supportare il controllo DirSync. Questo attributo contiene l'objectGuid dell'elemento padre di un oggetto quando si replica la creazione, la ridenominazione o lo spostamento di un oggetto.



| Voce | Valore |
|-------------------|-------------------------------------------------------|
| CN                | GUID padre                                           |
| Ldap-Display-Name | parentGUID                                            |
| Dimensione              | 16 byte                                              |
| Aggiorna privilegio  | Questo valore viene impostato dal sistema.                      |
| Frequenza di aggiornamento  | Durante la replica                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1224                               |
| System-Id-Guid    | 2df90d74-009f-11d2-aa4c-00c04fd7d83a                  |
| Sintassi            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|--------------|
| ID collegamento                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vero         |
| A valore singolo       | Vero         |
| Indicizzato             | Falso        |
| Nel catalogo globale      | Falso        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classi usate in        | \-           |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------|
| ID collegamento                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vero         |
| A valore singolo       | Vero         |
| Indicizzato             | Falso        |
| Nel catalogo globale      | Falso        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classi usate in        | \-           |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|--------------|
| ID collegamento                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vero         |
| A valore singolo       | Vero         |
| Indicizzato             | Falso        |
| Nel catalogo globale      | Falso        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classi usate in        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------|
| ID collegamento                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vero         |
| Is-Single-Valued       | Vero         |
| Indicizzato             | Falso        |
| Nel catalogo globale      | Falso        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classi usate in        | \-           |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------|
| ID collegamento                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vero         |
| Is-Single-Valued       | Vero         |
| Indicizzato             | Falso        |
| Nel catalogo globale      | Falso        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classi usate in        | \-           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------|
| ID collegamento                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vero         |
| Is-Single-Valued       | Vero         |
| Indicizzato             | Falso        |
| Nel catalogo globale      | Falso        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classi usate in        | \-           |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------|
| ID collegamento                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vero         |
| Is-Single-Valued       | Vero         |
| Indicizzato             | Falso        |
| Nel catalogo globale      | Falso        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classi usate in        | \-           |



 

 




