---
description: Indica il percorso di un archivio certificati.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Enumerazione CAPICOM_STORE_LOCATION (CAPICOM. h)
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
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331050"
---
# <a name="capicom_store_location-enumeration"></a>\_Enumerazione percorso archivio CAPICOM \_

Il tipo di enumerazione del **\_ \_ percorso dell'archivio CAPICOM** indica il percorso di un [*archivio certificati*](../secgloss/c-gly.md).

## <a name="members"></a>Membri



| Membro                                      | Descrizione                                                                                                                                                                                                                                                                      | Valore |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_Archivio di memoria CAPICOM \_**                  | L'archivio è un archivio di memoria. Eventuali modifiche apportate al contenuto dell'archivio non vengono rese permanente.<br/>                                                                                                                                                                              | 0     |
| **\_Archivio del computer locale \_ CAPICOM \_**          | L'archivio è un archivio del computer locale. Gli archivi di computer locali possono essere archivi di lettura/scrittura solo se l'utente dispone di autorizzazioni di lettura/scrittura. Se l'utente dispone di autorizzazioni di lettura/scrittura e se l'archivio è aperto in lettura/scrittura, le modifiche apportate al contenuto dell'archivio vengono rese permanente.<br/> | 1     |
| **\_ \_ archivio utente corrente CAPICOM \_**           | L'archivio è un archivio utente corrente. Un archivio utente corrente può essere un archivio di lettura/scrittura. In caso contrario, le modifiche apportate al contenuto dell'archivio vengono rese permanente.<br/>                                                                                                                      | 2     |
| **\_archivio utenti di Active \_ directory \_ di \_ CAPICOM** | L'archivio è un archivio Active Directory. Gli archivi di Active Directory possono essere aperti solo in modalità di sola lettura. I certificati non possono essere aggiunti o rimossi dagli archivi Active Directory.<br/>                                                                                        | 3     |
| **\_ \_ \_ archivio utenti smart card \_ CAPICOM**       | Gli archivi supportano gli archivi certificati basati su smart card. L'archivio è il gruppo di smart card presenti. Introdotta in capicol 2,0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione del **\_ \_ percorso dell'archivio CAPICOM** viene usato dai metodi seguenti:

-   [**PrivateKey. Open**](privatekey-open.md)
-   [**Store. Open**](store-open.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
