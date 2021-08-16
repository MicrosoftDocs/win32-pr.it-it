---
description: Le proprietà vengono usate per associare un valore a un certificato.
ms.assetid: a6433416-fe77-4bb0-bd8e-9410a49ab861
title: Funzioni di proprietà esterne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40196f4f42823ad44debeccc0fa85dc4615d58d1a0ccf521b2dd796e72574db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779631"
---
# <a name="external-property-functions"></a>Funzioni di proprietà esterne

Le proprietà vengono usate per associare un valore a un certificato. Le proprietà non vengono mai inviate o elaborate da [*un'autorità*](/windows/desktop/SecGloss/c-gly) di certificazione (CA) e non vengono archiviate all'interno di un certificato. In genere, vengono associati a un certificato dopo che il certificato è stato ricevuto dalla CA e prima che venga salvato in un archivio. Le proprietà vengono salvate nell'archivio insieme al certificato. CertEnroll.dll implementa [**l'interfaccia ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) e le interfacce seguenti derivate da **ICertProperty**:

-   [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)
-   [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)
-   [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)
-   [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)
-   [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)
-   [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)
-   [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)
-   [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)
-   [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)
-   [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)
-   [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)

Ognuna delle sezioni seguenti identifica una funzione esportata da Xenroll.dll per gestire le proprietà del certificato esterno. Ogni sezione illustra anche come usare CertEnroll.dll per sostituire la funzione o indica che non esiste alcun mapping tra le due librerie:

-   [addBlobPropertyToCertificateWStr](#addblobpropertytocertificatewstr)
-   [GetPrivateKeyArchiveCertificate](#getprivatekeyarchivecertificate)
-   [resetBlobProperties](#resetblobproperties)
-   [SetPrivateKeyArchiveCertificate](#setprivatekeyarchivecertificate)
-   [SetSignerCertificate](#setsignercertificate)
-   [Identificazione personaleWStr](#thumbprintwstr)
-   [Argomenti correlati](#related-topics)

## <a name="addblobpropertytocertificatewstr"></a>addBlobPropertyToCertificateWStr

La [**funzione addBlobPropertyToCertificateWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addblobpropertytocertificatewstr) in Xenroll.dll aggiunge una proprietà al certificato.

In CertEnroll.dll, tutti gli oggetti derivati da [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) implementano un [**metodo SetValueOnCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-setvalueoncertificate) che è possibile usare per associare una proprietà a un certificato. Inoltre, [**l'oggetto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) implementa direttamente le [**proprietà CertificateFriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname) [**e CertificateDescription.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatedescription)

## <a name="getprivatekeyarchivecertificate"></a>GetPrivateKeyArchiveCertificate

La [**funzione GetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprivatekeyarchivecertificate) in Xenroll.dll recupera il certificato di scambio usato per archiviare una [*chiave privata.*](/windows/desktop/SecGloss/p-gly)

È possibile usare [**l'oggetto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) in CertEnroll.dll creare una richiesta a una CA di archiviare la chiave privata. È necessario recuperare un certificato di [](/windows/desktop/SecGloss/p-gly) scambio dalla CA e usare la chiave pubblica contenuta in tale certificato per crittografare la chiave privata che si sta inviando per l'archiviazione. Per specificare o recuperare un certificato di scambio ca, chiamare la [**proprietà KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) su tale oggetto.

## <a name="resetblobproperties"></a>resetBlobProperties

La [**funzione resetBlobProperties**](/windows/desktop/api/xenroll/nf-xenroll-icenroll4-resetblobproperties) in Xenroll.dll rimuove la raccolta di proprietà dal certificato.

In CertEnroll.dll, tutti gli oggetti proprietà derivati da [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) implementano la [**proprietà RemoveFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-removefromcertificate) che è possibile usare per dissociare una proprietà da un certificato.

## <a name="setprivatekeyarchivecertificate"></a>SetPrivateKeyArchiveCertificate

La [**funzione SetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setprivatekeyarchivecertificate) in Xenroll.dll specifica un certificato di scambio usato per archiviare una chiave privata.

È possibile usare [**l'oggetto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) in CertEnroll.dll creare una richiesta a una CA di archiviare la chiave privata. È necessario recuperare un certificato di scambio dalla CA e usare la chiave pubblica contenuta in tale certificato per crittografare la chiave privata che si sta inviando per l'archiviazione. Per specificare o recuperare un certificato di scambio ca, chiamare la [**proprietà KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) su tale oggetto.

## <a name="setsignercertificate"></a>SetSignerCertificate

La [**funzione SetSignerCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setsignercertificate) in Xenroll.dll specifica un certificato del firmatario.

[**L'oggetto ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) CertEnroll.dll può essere usato per firmare una richiesta di certificato [*PKCS \# 7,*](/windows/desktop/SecGloss/p-gly)CMC o [*autofirmata.*](/windows/desktop/SecGloss/c-gly) È possibile inizializzare l'oggetto usando un certificato di firma esistente e associarlo a una richiesta chiamando una delle proprietà seguenti:

-   [**SignerCertificates**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates) in [ **IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) in [ **IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate) in [ **IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)

Inoltre, se si inizializza una richiesta CMC da una richiesta interna e un modello o si inizializza una richiesta PKCS 7 da una richiesta esistente, è possibile impostare il \# certificato di firma.

## <a name="thumbprintwstr"></a>Identificazione personaleWStr

La [**funzione ThumbPrintWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_thumbprintwstr) in Xenroll.dll specifica o recupera il valore dell'hash del certificato.

In CertEnroll.dll, è possibile usare l'oggetto [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash) per recuperare un valore [*hash*](/windows/desktop/SecGloss/h-gly) ([*identificazione*](/windows/desktop/SecGloss/t-gly)personale ) creato chiamando il [**metodo InitializeFromCertificate.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
