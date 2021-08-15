---
description: Le interfacce seguenti possono essere usate per gestire le firme dei certificati e le chiavi pubbliche e private.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Firma del certificato e interfacce chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdfd4c76b0e73f2954780d797e092e6d8b7570ebaee082ef93319f74abc24e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902307"
---
# <a name="certificate-signature-and-key-interfaces"></a>Firma del certificato e interfacce chiave

Le interfacce seguenti possono essere usate per gestire le firme dei certificati e le chiavi pubbliche e private.



| Interfaccia                                                      | Descrizione                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Rappresenta un certificato di firma che consente di firmare una richiesta di certificato.                  |
| [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Gestisce una raccolta di [**oggetti ISignerCertificate.**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Rappresenta una chiave privata asimmetrica che può essere utilizzata per la crittografia, la firma e l'accordo di chiave. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Rappresenta una chiave pubblica in una coppia di chiavi pubblica/privata.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Rappresenta le informazioni utilizzate per firmare una richiesta di certificato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



