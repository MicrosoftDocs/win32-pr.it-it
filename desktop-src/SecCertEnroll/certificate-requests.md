---
description: L'SDK di registrazione certificati può essere usato per creare richieste di \# \# certificato autofirmato e PKCS 10, PKCS 7, CMC.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Richieste di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308124"
---
# <a name="certificate-requests"></a>Richieste di certificati

L'SDK di registrazione certificati può essere usato per creare richieste di \# \# certificato autofirmato e PKCS 10, PKCS 7, CMC. Ogni tipo di richiesta è rappresentato da una delle interfacce elencate nella tabella seguente. Tutte le interfacce di richiesta ereditano direttamente o indirettamente dall'interfaccia [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) . 

| Interfaccia                                                                        | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Rappresenta una \# richiesta PKCS 10. Questa interfaccia eredita da [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Rappresenta una \# richiesta PKCS 7. Questa interfaccia eredita da [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Rappresenta un certificato autofirmato. Questa interfaccia eredita da [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10). |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Rappresenta una richiesta CMC. Questa interfaccia eredita da [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).               |



 

Nella figura seguente viene illustrata la struttura di ereditarietà degli oggetti Request supportati dall'API di registrazione del certificato. Un oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) serve, direttamente o indirettamente, come classe di base per tutti gli oggetti richiesta disponibili.

![struttura di ereditarietà per le interfacce di richiesta](images/certificate-request-inheritance.png)

Indipendentemente dal tipo, una richiesta di certificato contiene informazioni sull'oggetto che effettua la richiesta, la chiave pubblica del soggetto, un set di attributi, un set di estensioni X. 509 versione 3 (che possono essere inviate come parte degli attributi) e una firma. Questi problemi sono trattati negli argomenti seguenti:

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

 

 



