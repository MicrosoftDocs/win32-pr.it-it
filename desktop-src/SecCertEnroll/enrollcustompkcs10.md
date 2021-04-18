---
description: Crea una richiesta PKCS \# 10 personalizzata, la invia a un'autorità di certificazione (CA) autonoma e installa il certificato emesso nell'archivio certificati.
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ad95f483d4bc82136865e94a70ad46e90e1c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308120"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

L'esempio enrollCustomPKCS10 crea una richiesta PKCS \# 10 personalizzata, la invia a un'autorità di certificazione (CA) autonoma e installa il certificato emesso nell'archivio certificati. Una CA autonoma non richiede Active Directory e non usa i modelli.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollCustomPKCS10

## <a name="discussion"></a>Discussione

Esempio enrollCustomPKCS10:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del soggetto del certificato X. 500, il nome del messaggio di posta elettronica (RFC822) e un identificatore di oggetto (EKU) di utilizzo chiavi avanzato. Ad esempio, è possibile specificare gli argomenti seguenti per la registrazione *user1@example.com* :
    -   Nome soggetto: "*CN = User1, DC = example, DC = com*"
    -   Nome RFC822: *user1@example.com*
    -   IDENTIFICATORE EKU di autenticazione client: 1.3.6.1.5.5.7.3.2
2.  Crea un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza per l'utente finale specificando il valore **ContextUser** dell'enumerazione [**X509CertificateEnrollmentContext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext) .
3.  Crea un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , usa l'oggetto per codificare il nome del soggetto in una matrice di byte e aggiunge la matrice all' \# oggetto della richiesta PKCS 10.
4.  Crea un oggetto [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) , lo inizializza usando l'identificatore di oggetto EKU (OID) specificato nella riga di comando, crea una raccolta [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) , aggiunge il nuovo oggetto **IObjectId** (EKU) alla raccolta, usa la raccolta per inizializzare un oggetto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) e aggiunge questo oggetto alla richiesta.
5.  Crea un oggetto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) , lo inizializza usando il nome RFC822 specificato nella riga di comando, crea una raccolta [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , aggiunge il nuovo oggetto **IAlternativeName** (RFC822 Name) alla raccolta, crea un oggetto [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) e aggiunge questo oggetto alla richiesta.
6.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando l'oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e recupera una stringa che contiene una richiesta con codifica Base64.
7.  Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.
8.  Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa più le stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta all'autorità di certificazione.
9.  Controlla lo stato dell'invio e, se la registrazione ha esito positivo, installa il certificato nell'archivio certificati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\#Richiesta PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
