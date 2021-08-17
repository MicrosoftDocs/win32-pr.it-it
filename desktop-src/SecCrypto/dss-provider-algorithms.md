---
description: Nella tabella seguente sono elencati gli algoritmi supportati dal provider del servizio di crittografia Microsoft DSS.
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: Algoritmi del provider DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a39b29ee38b929f9ee5495d04cf663a1458fee0921fe48b24569038a69f0ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767219"
---
# <a name="dss-provider-algorithms"></a>Algoritmi del provider DSS

Nella tabella seguente sono elencati gli algoritmi supportati dal provider del servizio di crittografia Microsoft DSS.



| ID algoritmo    | Descrizione                                 | Commenti                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ MD5       | Algoritmo di hash MD5.                      | Fornito solo per l'hashing.                                                                                      |
| CALG \_ SHA       | Algoritmo di hash SHA.                      | Deve essere usato per le firme DSS.                                                                                |
| CALG \_ SHA1      | Uguale a CALG \_ SHA.                          | Nessun commento.                                                                                                     |
| CALG \_ DSS \_ SIGN | Algoritmo di firma della chiave pubblica/privata DSS. | Lunghezza chiave: può essere impostata, da 512 bit a 1.024 bit in incrementi di 64 bit. Lunghezza predefinita della chiave: 1.024 bit.<br/> |



 

 

 




