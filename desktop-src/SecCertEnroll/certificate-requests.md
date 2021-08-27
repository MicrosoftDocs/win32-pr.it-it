---
description: Certificate Enrollment SDK può essere usato per creare richieste di certificato \# PKCS 10, PKCS \# 7, CMC e autofirmate.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Richieste di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39125774584d127e40b16dbb2adca563d8c341b79454235163be30edc865b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902416"
---
# <a name="certificate-requests"></a>Richieste di certificato

Certificate Enrollment SDK può essere usato per creare richieste di certificato \# PKCS 10, PKCS \# 7, CMC e autofirmate. Ogni tipo di richiesta è rappresentato da una delle interfacce elencate nella tabella seguente. Tutte le interfacce di richiesta ereditano direttamente o indirettamente [**dall'interfaccia IX509CertificateRequest.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) 

| Interfaccia                                                                        | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Rappresenta una richiesta PKCS \# 10. Questa interfaccia eredita da [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Rappresenta una richiesta PKCS \# 7. Questa interfaccia eredita da [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Rappresenta un certificato autofirmato. Questa interfaccia eredita da [**IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Rappresenta una richiesta CMC. Questa interfaccia eredita da [**IX509CertificateRequestPkcs7.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               |



 

La figura seguente mostra la struttura di ereditarietà degli oggetti richiesta supportati dall'API di registrazione certificati. Un [**oggetto IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) funge direttamente o indirettamente da classe di base per tutti gli oggetti richiesta disponibili.

![Struttura di ereditarietà per le interfacce di richiesta](images/certificate-request-inheritance.png)

Indipendentemente dal tipo, una richiesta di certificato contiene informazioni sull'oggetto che effettua la richiesta, la chiave pubblica del soggetto, un set di attributi, un set di estensioni X.509 versione 3 (che possono essere inviate come parte degli attributi) e una firma. Questi problemi sono risolti dagli argomenti seguenti:

-   [Nomi soggetto](subject-names.md)
-   [Attributes (Attributi)](attributes.md)
-   [Estensioni](extensions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



