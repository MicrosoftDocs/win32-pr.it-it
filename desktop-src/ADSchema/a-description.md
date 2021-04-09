---
title: Attributo Description (schema AD)
description: Contiene la descrizione da visualizzare per un oggetto. Questo valore viene limitato come valore singolo per la compatibilità con le versioni precedenti in alcuni casi, ma può essere multivalore in altri. Vedere la sezione Osservazioni.
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo Description
- Schema di AD dell'attributo Description
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ccb155c9c65a42c29a022a6912b7aea7087477
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744274"
---
# <a name="description-attribute-ad-schema"></a>Attributo Description (schema AD)

Contiene la descrizione da visualizzare per un oggetto. Questo valore viene limitato come valore singolo per la compatibilità con le versioni precedenti in alcuni casi, ma può essere multivalore in altri. Vedere la sezione Osservazioni.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Descrizione                                 |
| LDAP-Display-Name | description                                 |
| Dimensione              | \-                                          |
| Privilegio aggiornamento  | Amministratore di dominio o proprietario dell'account.      |
| Frequenza di aggiornamento  | Ogni volta che è necessario modificare la descrizione.   |
| Attribute-Id      | 2.5.4.13                                    |
| System-ID-GUID    | bf967950-0de6-11d0-a285-00aa003049e2        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                           |
| MAPI-Id                | 0x806F                                                                       |
| System-Only            | Falso                                                                        |
| È a valore singolo       | Falso                                                                        |
| Indicizzato             | Falso                                                                        |
| Nel catalogo globale      | Vero                                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| Classi utilizzate in        | [**Sam-dominio**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                         |
| MAPI-Id                | 0x806F                                                                                                                                     |
| System-Only            | Falso                                                                                                                                      |
| È a valore singolo       | Falso                                                                                                                                      |
| Indicizzato             | Falso                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classi utilizzate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x806F                          |
| System-Only            | Falso                           |
| È a valore singolo       | Falso                           |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**In alto**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>Commenti

L'attributo Description viene implementato come attributo multivalore nello schema per i casi in cui è consentito. Per un oggetto che non è una classe gestita da SAM, la descrizione è multivalore. Per un attributo che è una classe gestita da SAM, l'attributo Description è a valore singolo. Le classi gestite da SAM sono per elementi come le entità di sicurezza, quindi, se si dispone, ad esempio, di un contenitore o di una classe personalizzata, lo schema consentirà di usare più valori. Questo comportamento dell'attributo Description è relativo alla compatibilità con le versioni precedenti dei sistemi operativi precedenti perché l'attributo era presente nelle API SAM prima dell'esistenza di AD.

 

 





