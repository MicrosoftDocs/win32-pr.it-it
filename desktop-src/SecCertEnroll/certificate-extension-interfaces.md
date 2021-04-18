---
description: Per creare estensioni di certificato, è possibile usare le interfacce seguenti.
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: Interfacce di estensione del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c192ff7bc661c36ded8611628a1cd82dddca1697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526334"
---
# <a name="certificate-extension-interfaces"></a>Interfacce di estensione del certificato

Per creare estensioni di certificato, è possibile usare le interfacce seguenti.



| Interfaccia                                                                            | Descrizione                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | Rappresenta un'istanza di un'estensione **AlternativeNames** .                                                                                   |
| [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | Gestisce una raccolta di oggetti [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) .                                                                  |
| [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | Specifica un criterio di certificato che identifica lo scopo per il quale è possibile utilizzare il certificato.                                              |
| [**ICertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | Gestisce una raccolta di oggetti [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy) .                                                              |
| [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | Rappresenta un qualificatore che può essere associato a un criterio di certificato.                                                                       |
| [**IPolicyQualifiers**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | Gestisce una raccolta di oggetti [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier) .                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | Definisce un'estensione per una richiesta di certificato.                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | Specifica una o più forme nome alternativo per l'oggetto di un certificato.                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | Rappresenta un'estensione **AuthorityKeyIdentifier** .                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | Specifica se l'oggetto del certificato è un'autorità di certificazione e, in caso affermativo, la profondità della catena di autorità di certificazione subordinata. |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | Rappresenta una raccolta di termini di informazioni sui criteri.                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | Rappresenta una raccolta di identificatori di oggetto che indicano il modo in cui un certificato può essere utilizzato da un'applicazione.                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | Rappresenta una raccolta di identificatori di oggetto che identificano gli utilizzi previsti della chiave pubblica contenuta in un certificato.                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | Rappresenta le restrizioni sulle operazioni che possono essere eseguite dalla chiave pubblica contenuta nel certificato.                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | Gestisce una raccolta di oggetti [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | Rappresenta una raccolta che segnala le funzionalità di decrittografia di un destinatario di posta elettronica a un mittente di posta elettronica.                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | Rappresenta un'estensione **SubjectKeyIdentifier** utilizzata per identificare un certificato di firma.                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | Rappresenta un'estensione **CertificateTemplate** che contiene un modello versione 2.                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | Rappresenta un'estensione **CertificateTemplateName** che contiene un modello versione 1.                                                         |
| [**ISmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | Gestisce una raccolta di oggetti [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability) .                                                                  |
| [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | Rappresenta un'estensione **SMIMECapabilities** che identifica le funzionalità di decrittografia di un destinatario di posta elettronica.                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



