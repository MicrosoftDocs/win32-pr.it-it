---
title: Extra-Columns attributo
description: Si tratta di un attributo multivalore i cui valori sono costituiti da 5 tupla (nome attributo), (titolo della colonna), (visibilità predefinita (0,1)), (larghezza della colonna ( \ 8211;1 per larghezza automatica)), 0 (riservato per uso futuro deve essere zero).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Extra-Columns schema AD dell'attributo
- Schema AD dell'attributo extraColumns
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6314a18ecac01a306c72d5879d191c5a744c20171495a3d57192078202d129f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177183"
---
# <a name="extra-columns-attribute"></a>Extra-Columns attributo

Si tratta di un attributo multivalore i cui valori sono costituiti da una tupla a 5: (nome dell'attributo), (titolo della colonna), (visibilità predefinita (0,1)), (larghezza della colonna ( 1 per larghezza automatica)), 0 (riservato per uso futuro deve essere zero). Questo valore viene usato dalla console Utenti e computer di Active Directory.



| Voce | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| Ldap-Display-Name | Extracolumns                                                                                                                                                         |
| Dimensione              | Ogni valore sarà la dimensione della stringa della 5 tupla precedente. Per impostazione predefinita, saranno presenti 22 valori nell'oggetto default-Display nel contenitore DisplaySpecifier. |
| Privilegio di aggiornamento  | Amministratore di dominio                                                                                                                                                 |
| Frequenza di aggiornamento  | Verrà aggiornato solo se è installato un servizio come Exchange.                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| System-Id-Guid    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Is-Single-Valued       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi usate in        | [**Identificatore di visualizzazione**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Is-Single-Valued       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi usate in        | [**Identificatore di visualizzazione**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Is-Single-Valued       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi usate in        | [**Identificatore di visualizzazione**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Is-Single-Valued       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi usate in        | [**Identificatore di visualizzazione**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Is-Single-Valued       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi usate in        | [**Identificatore di visualizzazione**](c-displayspecifier.md)<br/> |



 

 





