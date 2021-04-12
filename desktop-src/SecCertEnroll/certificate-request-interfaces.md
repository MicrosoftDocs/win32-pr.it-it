---
description: Per creare richieste di certificato, è possibile usare le interfacce seguenti.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Interfacce di richiesta di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129891"
---
# <a name="certificate-request-interfaces"></a>Interfacce di richiesta di certificato

Per creare richieste di certificato, è possibile usare le interfacce seguenti.



| Interfaccia                                                                          | Descrizione                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | Rappresenta l'interfaccia di primo livello astratta per una richiesta di certificato.                                                                                        |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | Consente di creare certificati direttamente senza passare attraverso un'autorità di certificazione o di registrazione.                                                  |
| [**IX509CertificateRequestCertificate2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | Estende l'interfaccia [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) per abilitare l'inizializzazione da un modello.              |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | Rappresenta una richiesta CMC.                                                                                                                                     |
| [**IX509CertificateRequestCmc2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | Estende l'interfaccia [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) per abilitare l'inizializzazione da un modello.                              |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | Rappresenta una \# richiesta PKCS 10.                                                                                                                               |
| [**IX509CertificateRequestPkcs10V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | Estende l'interfaccia [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) per abilitare l'inizializzazione da un modello.                        |
| [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | Estende l'interfaccia [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e aggiunge le proprietà che abilitano l'attestazione del certificato TPM. |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | Rappresenta una \# richiesta PKCS 7.                                                                                                                                |
| [**IX509CertificateRequestPkcs7V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | Estende l'interfaccia [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) per abilitare l'inizializzazione da un modello.                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



