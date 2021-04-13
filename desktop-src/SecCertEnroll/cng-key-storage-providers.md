---
description: "A differenza dell'API Cryptography (CryptoAPI), Cryptography API: Next Generation (CNG) separa i provider di crittografia da provider di archiviazione chiavi (KSP)."
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Provider di archiviazione chiavi CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401600"
---
# <a name="cng-key-storage-providers"></a>Provider di archiviazione chiavi CNG

A differenza dell'API Cryptography (CryptoAPI), Cryptography API: Next Generation (CNG) separa i provider di crittografia da provider di archiviazione chiavi (KSP). KSP può essere utilizzato per creare, eliminare, esportare, importare, aprire e archiviare chiavi. A seconda dell'implementazione, possono essere usati anche per la crittografia asimmetrica, il segreto e la firma. Microsoft installa i KSP seguenti a partire da Windows Vista e Windows Server 2008. I fornitori possono creare e installare altri provider.

## <a name="microsoft-software-key-storage-provider"></a>Provider di archiviazione chiavi del software Microsoft

Supporta la creazione e l'archiviazione delle chiavi software e gli algoritmi seguenti.



| Algoritmo                                          | Scopo                           | Lunghezza chiave (BITS)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Contratto segreto e scambio di chiave | da 512 a 4096 in incrementi di 64 bit  |
| Algoritmo di firma digitale (DSA)                  | Firme                        | da 512 a 1024 in incrementi di 64 bit  |
| Diffie-Hellman a curva ellittica (ECDH)               | Contratto segreto e scambio di chiave | P256, P384, P521                  |
| Algoritmo di firma digitale a curva ellittica (ECDSA) | Firme                        | P256, P384, P521                  |
| RSA                                                | Crittografia e firma asimmetrica | da 512 a 16384 in incrementi di 64 bit |



 

## <a name="microsoft-smart-card-key-storage-provider"></a>Provider di archiviazione chiavi per Smart Card Microsoft

Supporta la creazione e l'archiviazione delle chiavi smart card e gli algoritmi seguenti.



| Algoritmo                                          | Scopo                           | Lunghezza chiave (BITS)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Contratto segreto e scambio di chiave | da 512 a 4096 in incrementi di 64 bit  |
| Diffie-Hellman a curva ellittica (ECDH)               | Contratto segreto e scambio di chiave | P256, P384, P521                  |
| Algoritmo di firma digitale a curva ellittica (ECDSA) | Firme                        | P256, P384, P521                  |
| RSA                                                | Crittografia e firma asimmetrica | da 512 a 16384 in incrementi di 64 bit |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori dell'algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funzioni di archiviazione chiavi CNG](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[Informazioni sui provider di crittografia](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
