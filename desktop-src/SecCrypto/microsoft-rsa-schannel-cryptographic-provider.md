---
description: Il provider di crittografia Microsoft RSA/SChannel supporta l'hashing, la firma dei dati e la verifica della firma.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Provider di crittografia Microsoft RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9420849d62c0b728d8f3dbccc4210de3a1394308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966751"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a>Provider di crittografia Microsoft RSA/SChannel

Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) Cryptographic Provider supporta l'hashing, la firma dei dati e la verifica della firma. L'identificatore dell'algoritmo CALG \_ SSL3 \_ SHAMD5 viene usato per l'autenticazione client SSL 3,0 e TLS 1,0. Questo CSP supporta la derivazione delle chiavi per i protocolli SSL2, PCT1, SSL3 e TLS1. L' [*hash*](../secgloss/h-gly.md) è costituito da una concatenazione di un hash MD5 con un hash SHA e firmata con una [*chiave privata*](../secgloss/p-gly.md)RSA. Può essere esportato in altri paesi/aree geografiche.



|                |                                  |
|----------------|----------------------------------|
| Tipo di provider: | **DIMOSTRAZIONE di \_ RSA \_ Schannel**          |
| Nome provider: | **MS \_ def \_ RSA \_ Schannel \_ prov** |



 

Per ulteriori informazioni sui provider RSA/SChannel, vedere [funzioni CSP](cryptography-functions.md).

 

 
