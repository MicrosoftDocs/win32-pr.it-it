---
description: Crea un oggetto richiesta CMC da una richiesta PKCS 10 annidata interna \# .
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342731"
---
# <a name="createcngcustomcmc"></a>createCNGCustomCMC

L'esempio createCNGCustomCMC crea un oggetto richiesta CMC da una richiesta PKCS 10 annidata interna \# . La richiesta interna viene creata utilizzando una [*chiave privata*](/windows/desktop/SecGloss/p-gly)asimmetrica. La chiave privata viene creata usando il provider di crittografia CNG (Cryptography API: Next Generation) e l'algoritmo specificato nella riga di comando. Per la chiave privata vengono inoltre impostate opzioni personalizzate, ad esempio i criteri di esportazione e il livello di protezione delle chiavi.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ createCNGCustomCMC

## <a name="discussion"></a>Discussione

Esempio createCNGCustomCMC:

1.  Elabora gli argomenti della riga di comando seguenti:
    -   Nome di un provider del [*servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP) CNG.
    -   Nome dell'algoritmo utilizzato per generare una chiave privata asimmetrica.
    -   Nome dell'algoritmo utilizzato per eseguire l' [*hashing*](/windows/desktop/SecGloss/h-gly) della [*richiesta di certificato*](/windows/desktop/SecGloss/c-gly).
    -   Un file di output in cui salvare la richiesta di certificato.
    -   Stringa facoltativa (AlternateSignature) che, se presente, specifica che deve essere utilizzato un algoritmo discreto anziché un algoritmo di firma combinato. Per ulteriori informazioni, vedere la proprietà [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .
2.  Crea un oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e imposta le proprietà seguenti:
    -   [**LegacyCsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Algoritmo**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**Protezione di dati**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Crea una chiave privata asimmetrica.
4.  Crea un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza usando la chiave privata.
5.  Crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza usando l' \# oggetto richiesta PKCS 10 creato nel passaggio 4.
6.  Imposta il flag dell'algoritmo di firma alternativo su **Variant \_ true** o **Variant \_ false** a seconda che nella riga di comando sia specificata una stringa di firma alternativa. Per ulteriori informazioni, vedere [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).
7.  Crea un [*identificatore di oggetto*](/windows/desktop/SecGloss/o-gly) (OID) dell' [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) dal nome dell'algoritmo specificato nella riga di comando e imposta l'OID nell'oggetto della richiesta CMC.
8.  Firma la richiesta di certificato e la codifica usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).
9.  Recupera una stringa che contiene la richiesta di certificato CMC codificata e la Salva in un file. La funzione EncodeToFileW è definita in EnrollCommon. cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[\#Richiesta PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
