---
description: Gli algoritmi potrebbero essere supportati dal provider di crittografia Microsoft RSA/SChannel.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algoritmi del provider RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307667"
---
# <a name="rsaschannel-provider-algorithms"></a>Algoritmi del provider RSA/SChannel

Gli algoritmi seguenti potrebbero essere supportati da Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.



| ID algoritmo    | Descrizione                                                                                                                         | Commenti                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ RSA \_ KEYX | [ *Algoritmo di scambio delle chiavi* chiave pubblica RSA](../secgloss/k-gly.md) | Lunghezza della chiave: è possibile impostare 384 bit su 16.384 bit in incrementi di 8 bit. Lunghezza chiave predefinita: 1.024 bit.<br/> |
| \_MD5 CALG       | Algoritmo di hash MD5.                                                                                                              | Fornito solo per l'hashing.                                                                                      |
| \_Sha CALG       | Algoritmo di hash SHA.                                                                                                              | Deve essere usato per le firme DSS.                                                                                |
| CALG \_ RC2       | Algoritmo di crittografia a blocchi RC2.                                                                                                     | Lunghezza della chiave: da 40 a 88 bit                                                                                       |
| CALG \_ RC4       | Algoritmo di crittografia del flusso RC4.                                                                                                    | Lunghezza della chiave: da 40 a 88 bit                                                                                       |



 

 

 
