---
description: Le interfacce seguenti possono essere usate per creare attributi del certificato.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Interfacce degli attributi del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63cbd7b5e80fbb787a0d2aadcfb1617cb7972d7eed200da9184607ad0598031e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902924"
---
# <a name="certificate-attribute-interfaces"></a>Interfacce degli attributi del certificato

Le interfacce seguenti possono essere usate per creare attributi del certificato.



| Interfaccia                                                                    | Descrizione                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | Rappresenta un attributo di crittografia in una richiesta di certificato.                                                                              |
| [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | Gestisce una raccolta di [**oggetti ICryptAttribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                                                 |
| [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | Rappresenta un attributo in una richiesta di certificato \# PKCS 7, PKCS \# 10 o CMC.                                                               |
| [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | Rappresenta un attributo che può essere utilizzato per identificare il client che ha generato una richiesta di certificato.                                       |
| [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | Rappresenta le estensioni del certificato in una richiesta di certificato.                                                                             |
| [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | Rappresenta un attributo che contiene una chiave privata crittografata che deve essere archiviata da un'autorità di certificazione.                                 |
| [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | Rappresenta un attributo che contiene un hash SHA-1 della chiave privata crittografata da archiviare da un'autorità di certificazione.                |
| [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | Rappresenta un attributo che identifica il provider di crittografia utilizzato dall'entità che richiede il certificato.                           |
| [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | Rappresenta un attributo che contiene informazioni sulla versione del sistema operativo client in cui è stata generata la richiesta di certificato. |
| [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | Rappresenta un attributo che contiene il certificato da rinnovare.                                                                        |
| [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | Gestisce una raccolta di [**oggetti IX509Attribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                                                   |
| [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | Rappresenta una coppia nome-valore generica.                                                                                                       |
| [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | Gestisce una raccolta di [**oggetti IX509NameValuePair.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



