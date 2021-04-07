---
description: Supporta le firme digitali e la crittografia dei dati. Viene considerato un provider del servizio di crittografia (CSP) per utilizzo generico.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057962"
---
# <a name="prov_rsa_aes"></a>PROVA \_ \_ AES RSA

Il \_ tipo di \_ provider AES RSA di prova supporta sia le [firme digitali](digital-signatures.md) sia la crittografia dei dati. Viene considerato un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per utilizzo generico. L' [*algoritmo di chiave pubblica*](../secgloss/p-gly.md) RSA viene utilizzato per tutte le operazioni con [*chiave pubblica*](../secgloss/p-gly.md) .

## <a name="algorithms-supported"></a>Algoritmi supportati

Per le descrizioni di ognuno di questi algoritmi, vedere il glossario.



| Scopo      | Algoritmi supportati                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scambio di chiave | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Firma    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Crittografia   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) <br/>                                                       |
| Hashing      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-2 (SHA-256, SHA-384 e SHA-512)<br/> |



 

## <a name="related-documentation"></a>Related Documentation (Documentazione correlata)

Questo tipo di provider è definito da Microsoft e dalla sicurezza dei dati RSA. Viene descritto nei documenti seguenti:

-   *Guida per programmatori del provider del servizio di crittografia Microsoft*, microsoft, 1996.
-   RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi o aree geografiche.

 

 

 
