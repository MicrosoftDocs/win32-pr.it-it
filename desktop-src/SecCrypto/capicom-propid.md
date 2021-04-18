---
description: Definisce gli identificatori della proprietà CAPICOM.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: Enumerazione CAPICOM_PROPID (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROPID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d817262b869ef694c2cf9ff5b1e577840c3168a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326977"
---
# <a name="capicom_propid-enumeration"></a>CAPICOM propid ( \_ enumerazione)

L'enumerazione **CAPICOM \_ propid** definisce gli identificatori di proprietà CAPICOM.

## <a name="members"></a>Membri



| Membro                                                 | Descrizione                                                                                                                                                                                                                                                                                | Valore      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ propid \_ sconosciuto**                           | Il tipo della proprietà non è noto.<br/>                                                                                                                                                                                                                                          | 0          |
| **HANDLE di capicot \_ propid \_ chiave \_ prov \_**                 | Handle per un contenitore di chiavi all'interno di un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).<br/>                                                                                        | 1          |
| **CAPICOM \_ propid \_ chiave \_ prova \_ informazioni**                   | Informazioni su un contenitore di chiavi all'interno di un CSP.<br/>                                                                                                                                                                                                                                 | 2          |
| **\_ \_ Hash SHA1 propid di CAPICOM \_**                        | Oggetto hash SHA1.<br/>                                                                                                                                                                                                                                                             | 3          |
| **\_ \_ prop propid hash \_ prop**                        | Proprietà di un oggetto hash.<br/>                                                                                                                                                                                                                                                | 3          |
| **\_ \_ Hash MD5 propid di CAPICOM \_**                         | Oggetto hash MD5.<br/>                                                                                                                                                                                                                                                             | 4          |
| **contesto della chiave capicol \_ propid \_ \_**                      | [*Contesto*](../secgloss/c-gly.md)della chiave.<br/>                                                                                                                                                                                                | 5          |
| **specifiche della chiave capicol \_ propid \_ \_**                         | Specifiche per una chiave.<br/>                                                                                                                                                                                                                                                   | 6          |
| **CAPICOM \_ propid \_ Ie30 \_ riservato**                    | Informazioni sul fatto che l'oggetto sia riservato in Internet Explorer 3,0.<br/>                                                                                                                                                                                                      | 7          |
| **CAPICOM \_ propid \_ PUBKEY \_ hash \_ riservato**            | Informazioni che indica se l'hash della chiave pubblica è riservato.<br/>                                                                                                                                                                                                               | 8          |
| **utilizzo di capicol \_ propid \_ ENHKEY \_**                     | [*Utilizzo chiavi avanzato*](../secgloss/e-gly.md) (EKU).<br/>                                                                                                                                                              | 9          |
| **utilizzo di CAPICOM \_ propid \_ CTL \_**                        | Utilizzo di un [*elenco di certificati attendibili*](../secgloss/c-gly.md) (CTL).<br/>                                                                                                                                             | 9          |
| **\_ \_ \_ percorso di aggiornamento successivo \_ di CAPICOM propid**            | Percorso del successivo aggiornamento dell' [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               | 10         |
| **\_ \_ nome descrittivo propid di CAPICOM \_**                    | Nome leggibile.<br/>                                                                                                                                                                                                                                                          | 11         |
| **FILE capicol \_ propid \_ PVK \_**                         | Un file che contiene una chiave privata.<br/>                                                                                                                                                                                                                                             | 12         |
| **CAPICOM \_ propid \_ Descrizione**                       | Descrizione leggibile.<br/>                                                                                                                                                                                                                                                   | 13         |
| **stato di accesso di CAPICOM \_ propid \_ \_**                     | Stato dell'accesso.<br/>                                                                                                                                                                                                                                                        | 14         |
| **\_ \_ hash della firma CAPICOM propid \_**                   | Hash della firma.<br/>                                                                                                                                                                                                                                                        | 15         |
| **\_ \_ dati della smart card propid \_ di \_ CAPICOM**                 | Dati della smart card.<br/>                                                                                                                                                                                                                                                                | 16         |
| **\_propid \_ EFS**                               | Un [*Encrypting File System*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **dati di capicol \_ propid \_ fortezza \_**                    | Dati creati usando i protocolli di crittografia e gli algoritmi di proprietà del [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/> | 18         |
| **CAPICOM \_ propid \_ archiviato**                          | Informazioni sull'eventuale archiviazione dell'oggetto.<br/>                                                                                                                                                                                                                               | 19         |
| **identificatore di chiave capicol \_ propid \_ \_**                   | Identificatore di chiave.<br/>                                                                                                                                                                                                                                                               | 20         |
| **\_ \_ registrazione automatica di CAPICOM propid \_**                      | Informazioni di registrazione automatica per un certificato.<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ propid \_ PUBKEY \_ ALG \_ para**                 | Parametri per un algoritmo a chiave pubblica.<br/>                                                                                                                                                                                                                                          | 22         |
| **\_punti di dist propid \_ Cross \_ CERT \_ \_**         | Informazioni utilizzate per aggiornare i certificati incrociati dinamici.<br/>                                                                                                                                                                                                                          | 23         |
| **L' \_ \_ \_ \_ \_ hash MD5 della chiave pubblica dell'autorità emittente \_ propid CAPICOM**    | Hash MD5 della chiave pubblica dell'autorità emittente.<br/>                                                                                                                                                                                                                                        | 24         |
| **L' \_ \_ \_ \_ \_ hash MD5 della chiave pubblica del soggetto CAPICOM propid \_**   | Hash MD5 della chiave pubblica dell'oggetto.<br/>                                                                                                                                                                                                                                       | 25         |
| **\_registrazione propid CAPICOM \_**                        | Informazioni sulla registrazione del certificato.<br/>                                                                                                                                                                                                                                 | 26         |
| **\_indicatore di data propid \_ CAPICOM \_**                       | Indicatore di data.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **Il numero di \_ \_ serie dell'emittente \_ propid \_ \_ di CAPICOM \_** | Hash MD5 del numero di serie dell'emittente.<br/>                                                                                                                                                                                                                                     | 28         |
| **\_Nome del soggetto propid \_ \_ \_ di \_ CAPICOM**          | Hash MD5 del nome del soggetto.<br/>                                                                                                                                                                                                                                             | 29         |
| **\_ \_ informazioni sugli errori estesi di CAPICOM propid \_ \_**             | Informazioni estese su un errore.<br/>                                                                                                                                                                                                                                            | 30         |
| **\_rinnovo propid di CAPICOM \_**                           | Informazioni sul rinnovo di un' [*autorità di certificazione*](../secgloss/c-gly.md).<br/>                                                                                                                     | 64         |
| **\_ \_ \_ hash della chiave archiviato \_ di CAPICOM propid**               | Hash archiviato di una chiave.<br/>                                                                                                                                                                                                                                                      | 65         |
| **CAPICOM \_ propid \_ primo \_ riservato**                   | Informazioni sulla prima prenotazione.<br/>                                                                                                                                                                                                                                        | 66         |
| **\_ \_ ultimo riservato di CAPICOM propid \_**                    | Informazioni sulla prenotazione più recente.<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **CAPICOM \_ propid \_ primo \_ utente**                       | Informazioni sul primo utente.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **\_ \_ ultimo utente di CAPICOM propid \_**                        | Informazioni sull'utente più recente.<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalle proprietà di CAPICOM seguenti:

-   [**ExtendedProperty. PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties. Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
