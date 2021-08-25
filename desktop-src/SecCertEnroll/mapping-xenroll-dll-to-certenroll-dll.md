---
description: La Xenroll.dll è stata rimossa dal sistema operativo e sostituita da CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Mapping Xenroll.dll a CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8cd2286823dbf8029896c8656807f614dc0e1994fda908cd9b13ec8ad24c7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993531"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Mapping Xenroll.dll a CertEnroll.dll

Prima di Windows Vista, il controllo di registrazione certificati è stato implementato in Xenroll.dll. La Xenroll.dll è stata rimossa dal sistema operativo e sostituita da CertEnroll.dll.

Xenroll ha tentato di implementare due set paralleli di interfacce. [**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)e [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) erano conformi all'automazione e compatibili con i linguaggi di scripting. Le interfacce corrispondenti,[**IEnroll,**](/windows/desktop/api/xenroll/nn-xenroll-ienroll) [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)e [**IEnroll4,**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)non potevano essere script, ma erano più convenienti per i programmatori C++. Con l'evoluzione, i due set di interfacce non sono rimasti sincronizzati. In particolare, il set di interfacce duali rappresentato più di recente da **ICEnroll4** definisce solo un subset delle funzionalità definite da **IEnroll4.**

CertEnroll.dll implementa un set più ampio e strutturato di interfacce COM conformi ad Automazione. Gli argomenti seguenti illustrano come Xenroll.dll mapping a CertEnroll.dll per diversi tipi di funzionalità.

-   [Funzioni di richiesta del certificato](certificate-request-functions.md)
-   [Funzioni di risposta del certificato](certificate-response-functions.md)
-   [Funzioni per attributi](attribute-functions.md)
-   [Funzioni di estensione](extension-functions.md)
-   [Funzioni di proprietà esterne](external-property-functions.md)
-   [Funzioni a chiave privata e pubblica](private-and-public-key-functions.md)
-   [Funzioni del provider del servizio di crittografia](cryptographic-service-provider-functions.md)
-   [Funzioni dell'archivio certificati](certificate-store-functions.md)
-   [Funzioni di gestione delle Exchange personali](personal-information-exchange-functions.md)
-   [Funzioni helper](helper-functions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
