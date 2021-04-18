---
description: Algoritmi supportati da Microsoft Base DSS e Diffie-Hellman provider di crittografia.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Algoritmi del provider di PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319350"
---
# <a name="prov_dss_dh-provider-algorithms"></a>Prove \_ del \_ provider DH di prova DSS

Nella tabella seguente sono elencati gli algoritmi supportati da Microsoft Base DSS e Diffie-Hellman provider di crittografia.



| ID algoritmo      | Descrizione                                 | Commenti                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| \_MD5 CALG         | Algoritmo di hash MD5.                      | Fornito solo per l'hashing.                                                                                      |
| \_Sha CALG         | Algoritmo di hash SHA.                      | Deve essere usato per le firme DSS.                                                                                |
| CALG \_ SHA1        | Uguale a CALG \_ Sha.                          | Nessun commento.                                                                                                     |
| \_firma CALG DSS \_   | Algoritmo di firma della chiave pubblica/privata DSS. | Lunghezza della chiave: è possibile impostare 512 bit su 1.024 bit in incrementi di 64 bit. Lunghezza chiave predefinita: 1.024 bit.<br/> |
| CALG \_ DH \_ SF      | Archiviare e trasmettere lo scambio delle chiavi D-H.         | Lunghezza della chiave: è possibile impostare 384 bit su 512 bit in incrementi di 8 bit. Lunghezza chiave predefinita: 512 bit.<br/>      |
| CALG \_ DH \_ EPHEM   | Scambio di chiavi temporaneo D-H.                 | Lunghezza della chiave: è possibile impostare 384 bit su 512 bit in incrementi di 8 bit. Lunghezza chiave predefinita: 512 bit.<br/>      |
| CALG \_ CYLINK \_ MEK | Variante a 40 bit di una chiave DES.              | Lunghezza della chiave: 40 bit.                                                                                            |



 

 

 




