---
description: Supporta sia le firme digitali che la crittografia dei dati. È considerato un provider del servizio di crittografia (CSP) per utilizzo generico.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796ac0b77b91b9cffebc6f04ae3812b1bc25aabd885295e7dd3e1715bb4efc04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901591"
---
# <a name="prov_rsa_aes"></a>PROV \_ RSA \_ AES

Il tipo di provider RSA AES PROV supporta sia le \_ firme digitali che la crittografia dei \_ dati. [](digital-signatures.md) È considerato un provider del [*servizio di crittografia*](../secgloss/c-gly.md) (CSP) per utilizzo generico. L'algoritmo [*a chiave pubblica*](../secgloss/p-gly.md) RSA viene usato per tutte le operazioni con [*chiave*](../secgloss/p-gly.md) pubblica.

## <a name="algorithms-supported"></a>Algoritmi supportati

Per le descrizioni di ognuno di questi algoritmi, vedere il glossario.



| Scopo      | Algoritmi supportati                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chiave Exchange | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Firma    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Crittografia   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) <br/>                                                       |
| Hashing      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-2 (SHA-256, SHA-384 e SHA-512)<br/> |



 

## <a name="related-documentation"></a>Related Documentation (Documentazione correlata)

Questo tipo di provider è definito da Microsoft e RSA Data Security. È descritto nei documenti seguenti:

-   *Microsoft Cryptographic Service Provider Programmer's Guide*, Microsoft, 1996.
-   RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, novembre 1993.

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi o aree geografiche.

 

 

 
