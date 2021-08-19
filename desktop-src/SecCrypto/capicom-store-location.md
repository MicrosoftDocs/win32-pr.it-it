---
description: Indica il percorso di un archivio certificati.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: CAPICOM_STORE_LOCATION di controllo (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 15aa93b70840e13901f88c40c715024ec33a835be14b7453da99aecae079b487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879011"
---
# <a name="capicom_store_location-enumeration"></a>Enumerazione CAPICOM \_ STORE \_ LOCATION

Il **tipo di enumerazione CAPICOM STORE \_ \_ LOCATION** indica il percorso di un [*archivio certificati.*](../secgloss/c-gly.md)

## <a name="members"></a>Membri



| Membro                                      | Descrizione                                                                                                                                                                                                                                                                      | Valore |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **ARCHIVIO DI \_ MEMORIA \_ CAPICOM**                  | L'archivio è un archivio di memoria. Eventuali modifiche al contenuto dell'archivio non vengono rese persistenti.<br/>                                                                                                                                                                              | 0     |
| **CAPICOM \_ LOCAL \_ MACHINE \_ STORE**          | L'archivio è un archivio del computer locale. Gli archivi di computer locali possono essere archivi di lettura/scrittura solo se l'utente dispone di autorizzazioni di lettura/scrittura. Se l'utente dispone di autorizzazioni di lettura/scrittura e se l'archivio è aperto in lettura/scrittura, le modifiche apportate al contenuto dell'archivio vengono rese persistenti.<br/> | 1     |
| **CAPICOM \_ CURRENT \_ USER \_ STORE**           | L'archivio è un archivio utente corrente. Un archivio utente corrente può essere un archivio di lettura/scrittura. In caso contrario, le modifiche apportate al contenuto dell'archivio vengono rese persistenti.<br/>                                                                                                                      | 2     |
| **CAPICOM \_ ACTIVE \_ DIRECTORY \_ USER \_ STORE** | L'archivio è un archivio di Active Directory. Gli archivi Active Directory possono essere aperti solo in modalità di sola lettura. Non è possibile aggiungere o rimuovere certificati da archivi Active Directory.<br/>                                                                                        | 3     |
| **ARCHIVIO UTENTI \_ DI SMART \_ CARD \_ CAPICOM \_**       | Gli archivi supportano smart card di certificati basati su certificati basati su . Lo store è il gruppo di smart card presenti. Introdotto in CAPICOM 2.0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Commenti

Il **tipo di enumerazione CAPICOM STORE \_ \_ LOCATION** viene usato dai metodi seguenti:

-   [**PrivateKey.Open**](privatekey-open.md)
-   [**Store.Open**](store-open.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
