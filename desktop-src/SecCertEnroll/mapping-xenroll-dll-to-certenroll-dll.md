---
description: La libreria Xenroll.dll è stata rimossa dal sistema operativo e sostituita da CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Mapping Xenroll.dll CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758060"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Mapping Xenroll.dll CertEnroll.dll

Prima di Windows Vista, il controllo di registrazione dei certificati veniva implementato in Xenroll.dll. La libreria Xenroll.dll è stata rimossa dal sistema operativo e sostituita da CertEnroll.dll.

Xenroll ha tentato di implementare due set paralleli di interfacce. [**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)e [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) sono conformi all'automazione e sono compatibili con i linguaggi di scripting. Le interfacce corrispondenti,[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)e [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4), non possono essere generate nello script, ma sono più utili per i programmatori C++. Man mano che si sono evoluti, i due set di interfacce non rimangono sincronizzati. In particolare, il set di interfacce duali rappresentate più di recente da **ICEnroll4** definisce solo un subset della funzionalità definita da **IEnroll4**.

CertEnroll.dll implementa un set più ampio e strutturato di interfacce COM compatibili con l'automazione. Negli argomenti seguenti viene illustrato come Xenroll.dll viene eseguito il mapping CertEnroll.dll per diversi tipi di funzionalità.

-   [Funzioni di richiesta di certificato](certificate-request-functions.md)
-   [Funzioni di risposta del certificato](certificate-response-functions.md)
-   [Funzioni attributo](attribute-functions.md)
-   [Funzioni di estensione](extension-functions.md)
-   [Funzioni di proprietà esterne](external-property-functions.md)
-   [Funzioni chiave privata e pubblica](private-and-public-key-functions.md)
-   [Funzioni del provider del servizio di crittografia](cryptographic-service-provider-functions.md)
-   [Funzioni dell'archivio certificati](certificate-store-functions.md)
-   [Funzioni scambio informazioni personali](personal-information-exchange-functions.md)
-   [Funzioni helper](helper-functions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
