---
description: L'interfaccia IX509CertificateRequestPkcs10V3 espone le proprietà seguenti.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: Proprietà di IX509CertificateRequestPkcs10V3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcc126c21ca5fee5e8d1c15dd2561439c7a35f0f6cef637177ff36160a22d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976221"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>Proprietà di IX509CertificateRequestPkcs10V3

[**L'interfaccia IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) espone le proprietà seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttestationEncryptionCertificate - proprietà**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | Certificato usato per crittografare i valori EKPUB ed EKCERT dal client. Questa proprietà deve essere impostata su un certificato valido concatenato a una radice del computer attendibile.<br/>                                                                                                                                                                                |
| [**AttestPrivateKey - proprietà**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | True se la chiave privata creata deve essere attestata; in caso contrario, false. Se true, è previsto che sia stata impostata la proprietà [**AttestationEncryptionCertificate.**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) <br/>                                                                                                        |
| [**ChallengePassword - proprietà**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | Password da usare quando si crea una richiesta con una richiesta di verifica. Per creare una richiesta senza una richiesta, non impostare la [**proprietà ChallengePassword.**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                                                                                                                                      |
| [**EncryptionAlgorithm - proprietà**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | Algoritmo di crittografia usato per crittografare i valori EKPUB ed EKCERT dal client.<br/>                                                                                                                                                                                                                                                               |
| [**EncryptionStrength - proprietà**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Identifica la lunghezza in bit [**dell'oggetto EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) da utilizzare per la crittografia. Se **EncryptionAlgorithm** supporta solo una lunghezza di bit, non è necessario specificare un valore per la [**proprietà EncryptionStrength.**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/> |
| [**NameValuePairs - proprietà**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Raccolta di coppie nome/valore di valori aggiuntivi delle proprietà del certificato.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




