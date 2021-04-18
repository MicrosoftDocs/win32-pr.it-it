---
description: Specifica il tipo di provider del servizio di crittografia (CSP).
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: Enumerazione CAPICOM_PROV_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROV_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d9c701b453656a68573fe391775c5b27fdd2461a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329736"
---
# <a name="capicom_prov_type-enumeration"></a>\_Enumerazione del tipo CApicot \_

L'enumerazione del **\_ \_ tipo capicol prov** specifica il tipo di [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

## <a name="members"></a>Membri



| Membro                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                        | Valore |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **capicol \_ prova \_ RSA \_ completo**       | Il CSP completo di [*RSA*](../secgloss/r-gly.md) . Questo tipo di provider supporta le [*firme digitali*](../secgloss/d-gly.md) e la [*crittografia*](../secgloss/e-gly.md)dei dati.<br/>                                                            | 1     |
| **capicol \_ prov \_ RSA \_ sig**        | Subset del CSP RSA che supporta solo le funzioni e gli algoritmi richiesti per gli hash e le firme digitali.<br/>                                                                                                                                                                                                                                        | 2     |
| **capicol \_ prov \_ DSS**             | Il CSP di [*Digital Signature standard*](../secgloss/d-gly.md) (DSS). Questo tipo di provider supporta solo hash e firme digitali. DSS usa l' [*algoritmo di firma digitale*](../secgloss/d-gly.md) (DSA).<br/> | 3     |
| **capicol \_ prova di \_ fortezza**        | CSP che contiene i protocolli e gli algoritmi di crittografia di proprietà del [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                      | 4     |
| **CAPICOM \_ provare \_ MS \_ Exchange**    | CSP progettato per le esigenze crittografiche di Exchange e di altre applicazioni compatibili con Microsoft Mail.<br/>                                                                                                                                                                                                                                       | 5     |
| **capicol \_ prova \_ SSL**             | CSP che supporta il protocollo [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ prova \_ RSA \_ Schannel**   | CSP che supporta sia i protocolli [*RSA*](../secgloss/r-gly.md) che i protocolli [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ prova \_ DSS \_ DH**         | CSP che supporta i protocolli DSS e [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                          | 13    |
| **capicol \_ prova \_ EC \_ ECDSA \_ sig**  | CSP che supporta le funzioni e gli algoritmi ECDSA (ellittica Digital Signature Algorithm) necessari per le firme digitali.<br/>                                                                                                                                                                                                                                  | 14    |
| **capicol \_ prova \_ EC \_ ECNRA \_ sig**  | CSP che supporta la curva ellittica Nyberg-Rueppel le funzioni analogiche (ECNRA) e gli algoritmi richiesti per le firme digitali.<br/>                                                                                                                                                                                                                                        | 15    |
| **capicol \_ prove \_ EC \_ ECDSA \_ completo** | CSP che supporta il ECDSA completo.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **capicol \_ prove \_ EC \_ ECNRA \_ completo** | CSP che supporta il ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ prova \_ DH \_ Schannel**    | CSP che supporta sia i protocolli [*Diffie-Hellman*](../secgloss/d-gly.md) che i protocolli [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ prova \_ Spyrus Deployment \_ Lynks**   | CSP che supporta il dispositivo Spyrus Deployment LYNKS card.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **capicol \_ prov \_ RNG**             | CSP che gestisce la generazione di numeri casuali.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ prova \_ Intel \_ sec**      | CSP che fornisce la sicurezza di Intel.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM prova a \_ \_ sostituire \_ OWF**    | CSP che supporta la sostituzione del modo in cui vengono generati formati unidirezionali da password.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ prova \_ RSA \_ AES**        | CSP che supporta le firme digitali e la crittografia dei dati tramite l'algoritmo Advanced Encryption Standard ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Commenti

L'enumerazione di **\_ \_ tipo capicol prov** viene utilizzata dai metodi e dalle proprietà seguenti:

-   Proprietà [**PrivateKey. ProviderType**](privatekey-providertype.md) .
-   Metodo [**PrivateKey. Open**](privatekey-open.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
