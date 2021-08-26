---
description: Specifica il tipo di provider del servizio di crittografia (CSP).
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: CAPICOM_PROV_TYPE di controllo (Capicom.h)
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
ms.openlocfilehash: bf85d2eb01ffd4290c5200e09c842f280cd5418dc5203bba068ecb5bcd65c355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879021"
---
# <a name="capicom_prov_type-enumeration"></a>Enumerazione CAPICOM \_ PROV \_ TYPE

**L'enumerazione \_ CAPICOM PROV \_ TYPE** specifica il tipo di [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

## <a name="members"></a>Membri



| Membro                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                        | Valore |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ PROV \_ RSA \_ FULL**       | Provider di [*servizi di*](../secgloss/r-gly.md) configurazione RSA completo. Questo tipo di provider supporta sia [*le firme digitali che*](../secgloss/d-gly.md) la crittografia dei [*dati.*](../secgloss/e-gly.md)<br/>                                                            | 1     |
| **CAPICOM \_ PROV \_ RSA \_ SIG**        | Subset del provider di servizi di configurazione RSA che supporta solo le funzioni e gli algoritmi necessari per hash e firme digitali.<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ PROV \_ DSS**             | Provider di servizi di configurazione DSS [*(Digital Signature Standard).*](../secgloss/d-gly.md) Questo tipo di provider supporta solo hash e firme digitali. DSS usa [*l'algoritmo*](../secgloss/d-gly.md) DSA (Digital Signature Algorithm).<br/> | 3     |
| **CAPICOM \_ PROV \_ FORIONE**        | Provider di servizi di configurazione che contiene i protocolli e gli algoritmi di crittografia di proprietà del [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                      | 4     |
| **CAPICOM \_ PROV \_ MS \_ EXCHANGE**    | Provider di servizi di configurazione progettato per le esigenze di Exchange e altre applicazioni compatibili con Microsoft Mail.<br/>                                                                                                                                                                                                                                       | 5     |
| **CAPICOM \_ PROV \_ SSL**             | Provider di servizi di configurazione che [*supporta il protocollo Secure Sockets Layer*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ PROV \_ RSA \_ SCHANNEL**   | Provider di servizi di configurazione che supporta i [*protocolli RSA*](../secgloss/r-gly.md) [*e Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ PROV \_ DSS \_ DH**         | CSP che supporta i protocolli DSS e [*Diffie-Hellman.*](../secgloss/d-gly.md)<br/>                                                                                                                                                                                                          | 13    |
| **CAPICOM \_ PROV \_ EC \_ ECDSA \_ SIG**  | Provider di servizi di crittografia che supporta le funzioni e gli algoritmi ECDSA (Elliptic Curve Digital Signature Algorithm) necessari per le firme digitali.<br/>                                                                                                                                                                                                                                  | 14    |
| **CAPICOM \_ PROV \_ EC \_ ECNRA \_ SIG**  | CSP che supporta le funzioni e gli algoritmi ECNRA (Elliptic Curve Nyberg-Rueppel Analog) necessari per le firme digitali.<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM \_ PROV \_ EC \_ ECDSA \_ FULL** | CSP che supporta l'intero ECDSA.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **CAPICOM \_ PROV \_ EC \_ ECNRA \_ FULL** | CSP che supporta la versione completa di ECNRA.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ PROV \_ DH \_ SCHANNEL**    | CSP che supporta i protocolli [*Diffie-Hellman*](../secgloss/d-gly.md) [*e Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ PROV \_ SPYRUS \_ LYNKS**   | Provider di servizi di configurazione che supporta il dispositivo spyrus LYNKS Card.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ PROV \_ RNG**             | CSP che gestisce la generazione di numeri casuali.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ PROV \_ INTEL \_ SEC**      | Provider di servizi di configurazione che fornisce la sicurezza di Intel.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ PROV \_ REPLACE \_ OWF**    | CSP che supporta la sostituzione del modo in cui i formati unidireli vengono generati dalle password.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ PROV \_ RSA \_ AES**        | Provider di servizi di configurazione che supporta sia le firme digitali che la crittografia dei dati usando l'Advanced Encryption Standard [*(AES).*](../secgloss/a-gly.md)<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Commenti

**L'enumerazione \_ CAPICOM PROV \_ TYPE** viene usata dai metodi e dalle proprietà seguenti:

-   [**Proprietà PrivateKey.ProviderType.**](privatekey-providertype.md)
-   [**Metodo PrivateKey.Open.**](privatekey-open.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
