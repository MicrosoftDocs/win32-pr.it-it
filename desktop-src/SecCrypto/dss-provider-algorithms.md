---
description: La tabella seguente elenca gli algoritmi supportati dal provider di crittografia Microsoft DSS.
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: Algoritmi del provider DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0bd9346da7a9ab1490e2646d9d2559c07359b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311924"
---
# <a name="dss-provider-algorithms"></a>Algoritmi del provider DSS

La tabella seguente elenca gli algoritmi supportati dal provider di crittografia Microsoft DSS.



| ID algoritmo    | Descrizione                                 | Commenti                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| \_MD5 CALG       | Algoritmo di hash MD5.                      | Fornito solo per l'hashing.                                                                                      |
| \_Sha CALG       | Algoritmo di hash SHA.                      | Deve essere usato per le firme DSS.                                                                                |
| CALG \_ SHA1      | Uguale a CALG \_ Sha.                          | Nessun commento.                                                                                                     |
| \_firma CALG DSS \_ | Algoritmo di firma della chiave pubblica/privata DSS. | Lunghezza della chiave: è possibile impostare 512 bit su 1.024 bit in incrementi di 64 bit. Lunghezza chiave predefinita: 1.024 bit.<br/> |



 

 

 




