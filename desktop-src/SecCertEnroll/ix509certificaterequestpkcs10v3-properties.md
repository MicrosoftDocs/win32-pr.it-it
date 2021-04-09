---
description: L'interfaccia IX509CertificateRequestPkcs10V3 espone le proprietà seguenti.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: Proprietà di IX509CertificateRequestPkcs10V3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4967b10e49ed015b22ffcab19726f5662937d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968506"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>Proprietà di IX509CertificateRequestPkcs10V3

L'interfaccia [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) espone le proprietà seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Proprietà AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | Certificato utilizzato per crittografare i valori EKPUB e EKCERT dal client. Questa proprietà deve essere impostata su un certificato valido concatenato a una radice del computer attendibile.<br/>                                                                                                                                                                                |
| [**Proprietà AttestPrivateKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | True se è necessario attestare la chiave privata creata. in caso contrario, false. Se true, è previsto che sia stata impostata la proprietà [**AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) . <br/>                                                                                                        |
| [**Proprietà ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | Password da usare quando si crea una richiesta con una richiesta di verifica. Per creare una richiesta senza una richiesta di verifica, non impostare la proprietà [**ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword) .<br/>                                                                                                                                      |
| [**Proprietà EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | Algoritmo di crittografia utilizzato per crittografare i valori EKPUB e EKCERT dal client.<br/>                                                                                                                                                                                                                                                               |
| [**Proprietà livellocrittografia**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Identifica la lunghezza in bit del [**EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) da utilizzare per la crittografia. Se il **EncryptionAlgorithm** supporta solo una lunghezza di bit, non è necessario specificare un valore per la proprietà [**livellocrittografia**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength) .<br/> |
| [**Proprietà NameValuePairs**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Raccolta di coppie nome/valore di valori di proprietà del certificato aggiuntivi.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




