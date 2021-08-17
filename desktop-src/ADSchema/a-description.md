---
title: Attributo Description (schema AD)
description: Contiene la descrizione da visualizzare per un oggetto . Questo valore è limitato come a valore singolo per la compatibilità con le versioni precedenti in alcuni casi, ma può essere multivalore in altri. Vedere la sezione Osservazioni.
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Description
- Schema AD dell'attributo description
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f53c344b026a89a3f579d1eb7fc7002a8a0410d28fd9b43d05882a4285eb73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961729"
---
# <a name="description-attribute-ad-schema"></a>Attributo Description (schema AD)

Contiene la descrizione da visualizzare per un oggetto . Questo valore è limitato come a valore singolo per la compatibilità con le versioni precedenti in alcuni casi, ma può essere multivalore in altri. Vedere la sezione Osservazioni.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Descrizione                                 |
| Ldap-Display-Name | description                                 |
| Dimensione              | \-                                          |
| Privilegio di aggiornamento  | Amministratore di dominio o proprietario dell'account.      |
| Frequenza di aggiornamento  | Ogni volta che la descrizione deve cambiare.   |
| Attribute-Id      | 2.5.4.13                                    |
| System-Id-Guid    | bf967950-0de6-11d0-a285-00aa003049e2        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                           |
| MAPI-Id                | 0x806F                                                                       |
| System-Only            | Falso                                                                        |
| Is-Single-Valued       | Falso                                                                        |
| Indicizzato             | Falso                                                                        |
| Nel catalogo globale      | Vero                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| Classi usate in        | [**Sam-Domain**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                         |
| MAPI-Id                | 0x806F                                                                                                                                     |
| System-Only            | Falso                                                                                                                                      |
| Is-Single-Valued       | Falso                                                                                                                                      |
| Indicizzato             | Falso                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classi usate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x806F                          |
| System-Only            | Falso                           |
| Is-Single-Valued       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| A valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classi usate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| A valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classi usate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classi usate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classi usate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>Commenti

L'attributo description viene implementato come attributo multivalore nello schema per i casi in cui è consentito. Per un oggetto che non è una classe gestita SAM, la descrizione è multivalore. Per un attributo che è una classe gestita SAM, l'attributo description è a valore singolo. Le classi gestite SAM sono per aspetti come le entità di sicurezza, quindi, se si dispone, ad esempio, di un contenitore o di una classe personalizzata, lo schema consente di usare più valori. Questo comportamento dell'attributo description è per la compatibilità con le versioni precedenti dei sistemi operativi perché l'attributo esisteva nelle API SAM prima dell'esistenza di AD.

 

 





