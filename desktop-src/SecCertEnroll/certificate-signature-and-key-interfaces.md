---
description: Le interfacce seguenti possono essere utilizzate per gestire le firme dei certificati e le chiavi pubbliche e private.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Firma del certificato e interfacce chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883314"
---
# <a name="certificate-signature-and-key-interfaces"></a>Firma del certificato e interfacce chiave

Le interfacce seguenti possono essere utilizzate per gestire le firme dei certificati e le chiavi pubbliche e private.



| Interfaccia                                                      | Descrizione                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Rappresenta un certificato di firma che consente di firmare una richiesta di certificato.                  |
| [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Gestisce una raccolta di oggetti [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Rappresenta una chiave privata asimmetrica che può essere utilizzata per la crittografia, la firma e il contratto di chiave. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Rappresenta una chiave pubblica in una coppia di chiavi pubblica/privata.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Rappresenta le informazioni utilizzate per firmare una richiesta di certificato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



