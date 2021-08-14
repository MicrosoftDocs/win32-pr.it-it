---
description: Definisce gli identificatori di proprietà CAPICOM.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: CAPICOM_PROPID enumerazione (Capicom.h)
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
ms.openlocfilehash: 6d99c823d5396d2b8ece4484fa8888dff19b7898fb7d3b6ebedc5841b85c7e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772267"
---
# <a name="capicom_propid-enumeration"></a>Enumerazione \_ CAPICOM PROPID

**L'enumerazione \_ CAPICOM PROPID** definisce gli identificatori di proprietà CAPICOM.

## <a name="members"></a>Membri



| Membro                                                 | Descrizione                                                                                                                                                                                                                                                                                | Valore      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ PROPID \_ UNKNOWN**                           | Il tipo della proprietà non è noto.<br/>                                                                                                                                                                                                                                          | 0          |
| **HANDLE \_ \_ PROV DELLA CHIAVE PROPID CAPICOM \_ \_**                 | Handle per un contenitore di chiavi all'interno [*di un provider del servizio di*](../secgloss/c-gly.md) crittografia (CSP).<br/>                                                                                        | 1          |
| **INFORMAZIONI SUL \_ \_ \_ PROV DELLA CHIAVE PROPID CAPICOM \_**                   | Informazioni su un contenitore di chiavi all'interno di un provider di servizi di configurazione.<br/>                                                                                                                                                                                                                                 | 2          |
| **CAPICOM \_ PROPID \_ SHA1 \_ HASH**                        | Oggetto hash SHA1.<br/>                                                                                                                                                                                                                                                             | 3          |
| **PROPRIETÀ HASH \_ PROPID \_ CAPICOM \_**                        | Proprietà di un oggetto hash.<br/>                                                                                                                                                                                                                                                | 3          |
| **CAPICOM \_ PROPID \_ MD5 \_ HASH**                         | Oggetto hash MD5.<br/>                                                                                                                                                                                                                                                             | 4          |
| **CONTESTO DELLA CHIAVE PROPID CAPICOM \_ \_ \_**                      | Contesto della [*chiave.*](../secgloss/c-gly.md)<br/>                                                                                                                                                                                                | 5          |
| **SPECIFICA \_ DELLA CHIAVE PROPID \_ \_ CAPICOM**                         | Specifiche per una chiave.<br/>                                                                                                                                                                                                                                                   | 6          |
| **CAPICOM \_ PROPID \_ IE30 \_ RISERVATO**                    | Informazioni sulla riserva dell'oggetto in Internet Explorer 3.0.<br/>                                                                                                                                                                                                      | 7          |
| **HASH \_ \_ PUBKEY PROPID CAPICOM \_ \_ RISERVATO**            | Informazioni sulla riserva dell'hash della chiave pubblica.<br/>                                                                                                                                                                                                               | 8          |
| **UTILIZZO DI CAPICOM \_ PROPID \_ \_ ENHKEY**                     | Un [*utilizzo chiavi avanzato*](../secgloss/e-gly.md) (EKU).<br/>                                                                                                                                                              | 9          |
| **UTILIZZO CTL DI CAPICOM \_ PROPID \_ \_**                        | Utilizzo [*di un elenco di*](../secgloss/c-gly.md) certificati attendibili (CTL).<br/>                                                                                                                                             | 9          |
| **POSIZIONE DI AGGIORNAMENTO SUCCESSIVO DI CAPICOM \_ PROPID \_ \_ \_**            | Percorso dell'aggiornamento successivo [*all'elenco di revoche*](../secgloss/c-gly.md) di certificati (CRL).<br/>                                                                                               | 10         |
| **NOME DESCRITTIVO DI CAPICOM \_ PROPID \_ \_**                    | Nome leggibile dall'utente.<br/>                                                                                                                                                                                                                                                          | 11         |
| **CAPICOM \_ PROPID \_ PVK \_ FILE**                         | File che contiene una chiave privata.<br/>                                                                                                                                                                                                                                             | 12         |
| **DESCRIZIONE \_ DEL PROPID CAPICOM \_**                       | Descrizione leggibile dall'utente.<br/>                                                                                                                                                                                                                                                   | 13         |
| **STATO DI ACCESSO PROPID CAPICOM \_ \_ \_**                     | Stato dell'accesso.<br/>                                                                                                                                                                                                                                                        | 14         |
| **HASH DELLA FIRMA \_ PROPID CAPICOM \_ \_**                   | Hash della firma.<br/>                                                                                                                                                                                                                                                        | 15         |
| **DATI \_ DELLA \_ SMART \_ CARD CAPICOM PROPID \_**                 | Dati della smart card.<br/>                                                                                                                                                                                                                                                                | 16         |
| **CAPICOM \_ PROPID \_ EFS**                               | Un [*Encrypting File System*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **DATI DI CAPICOM \_ PROPID \_ FORTEZZA \_**                    | Dati creati usando i protocolli e gli algoritmi crittografici di proprietà del [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/> | 18         |
| **CAPICOM \_ PROPID \_ ARCHIVIATO**                          | Informazioni sull'archiviazione dell'oggetto.<br/>                                                                                                                                                                                                                               | 19         |
| **IDENTIFICATORE \_ DELLA CHIAVE PROPID CAPICOM \_ \_**                   | Identificatore di chiave.<br/>                                                                                                                                                                                                                                                               | 20         |
| **REGISTRAZIONE AUTOMATICA DI CAPICOM \_ PROPID \_ \_**                      | Informazioni di registrazione automatica per un certificato.<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ PARA**                 | Parametri per un algoritmo a chiave pubblica.<br/>                                                                                                                                                                                                                                          | 22         |
| **PUNTI DI DIST DEL CERTIFICATO INCROCIATO CAPICOM \_ PROPID \_ \_ \_ \_**         | Informazioni usate per aggiornare i certificati incrociati dinamici.<br/>                                                                                                                                                                                                                          | 23         |
| **HASH MD5 DELLA CHIAVE PUBBLICA DELL'AUTORITÀ DI \_ \_ \_ \_ \_ EMISSIONE DI \_ CAPICOM PROPID**    | Hash MD5 della chiave pubblica dell'autorità emittente.<br/>                                                                                                                                                                                                                                        | 24         |
| **HASH \_ \_ \_ \_ \_ MD5 DELLA CHIAVE PUBBLICA DEL \_ SOGGETTO DI CAPICOM PROPID**   | Hash MD5 della chiave pubblica dell'oggetto.<br/>                                                                                                                                                                                                                                       | 25         |
| **REGISTRAZIONE \_ PROPID CAPICOM \_**                        | Informazioni sulla registrazione del certificato.<br/>                                                                                                                                                                                                                                 | 26         |
| **STAMP \_ DI DATA PROPID CAPICOM \_ \_**                       | Indicatore di data.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **HASH MD5 DEL NUMERO DI SERIE DELL'AUTORITÀ DI \_ \_ \_ \_ \_ EMITTENTE CAPICOM \_ PROPID** | Hash MD5 del numero di serie dell'autorità emittente.<br/>                                                                                                                                                                                                                                     | 28         |
| **CAPICOM \_ PROPID \_ SUBJECT \_ NAME \_ MD5 \_ HASH**          | Hash MD5 del nome del soggetto.<br/>                                                                                                                                                                                                                                             | 29         |
| **INFORMAZIONI SULL'ERRORE ESTESO DI CAPICOM \_ PROPID \_ \_ \_**             | Informazioni estese su un errore.<br/>                                                                                                                                                                                                                                            | 30         |
| **RINNOVO \_ PROPID CAPICOM \_**                           | Informazioni sul rinnovo di [*un'autorità di certificazione.*](../secgloss/c-gly.md)<br/>                                                                                                                     | 64         |
| **CAPICOM \_ PROPID \_ ARCHIVED \_ KEY \_ HASH**               | Hash archiviato di una chiave.<br/>                                                                                                                                                                                                                                                      | 65         |
| **CAPICOM \_ PROPID \_ FIRST \_ RESERVED**                   | Informazioni sulla prima prenotazione.<br/>                                                                                                                                                                                                                                        | 66         |
| **CAPICOM \_ PROPID \_ LAST \_ RESERVED**                    | Informazioni sulla prenotazione più recente.<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **CAPICOM \_ PROPID \_ FIRST \_ USER**                       | Informazioni sul primo utente.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **CAPICOM \_ PROPID \_ LAST \_ USER**                        | Informazioni sull'utente più recente.<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalle proprietà CAPICOM seguenti:

-   [**ExtendedProperty.PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties.Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
