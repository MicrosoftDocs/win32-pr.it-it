---
description: Il formato del certificato X.509 versione 3 identifica più estensioni che possono essere aggiunte a un certificato per fornire informazioni avanzate sull'utilizzo delle chiavi, i criteri e i vincoli del certificato, i moduli dei nomi alternativi e altro ancora.
ms.assetid: d53107b7-a153-41cf-9876-1d28aaf99816
title: Funzioni di estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da84fbe58e4b3cdb3bd510b8ec33bedd0ab7af29f3c0a592724f2711bb9bedd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779864"
---
# <a name="extension-functions"></a>Funzioni di estensione

Il formato [*del certificato X.509*](/windows/desktop/SecGloss/x-gly) versione 3 identifica più estensioni che possono essere aggiunte a un certificato per fornire informazioni avanzate sull'utilizzo delle chiavi, i criteri e i vincoli del certificato, i moduli dei nomi alternativi e altro ancora.

CertEnroll.dll implementa le interfacce seguenti per gestire le estensioni del certificato:

-   [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
-   [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
-   [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)
-   [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)
-   [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)
-   [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)
-   [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)
-   [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)
-   [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)
-   [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)
-   [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)
-   [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)
-   [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

Ognuna delle sezioni seguenti illustra una funzione esportata da Xenroll.dll per gestire le estensioni del certificato. Ogni sezione illustra anche come usare CertEnroll.dll per sostituire la funzione o indica che non esiste alcun mapping tra le due librerie:

-   [AddCertTypeToRequestWStr](#addcerttypetorequestwstr)
-   [AddCertTypeToRequestWStrEx](#addcerttypetorequestwstrex)
-   [AddExtensionsToRequest](#addextensionstorequest)
-   [addExtensionToRequestWStr](#addextensiontorequestwstr)
-   [EnableSMIMECapabilities](#enablesmimecapabilities)
-   [IncludeSubjectKeyID](#includesubjectkeyid)
-   [resetExtensions](#resetextensions)
-   [Argomenti correlati](#related-topics)

## <a name="addcerttypetorequestwstr"></a>AddCertTypeToRequestWStr

La [**funzione AddCertTypeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr) in Xenroll.dll aggiunge un modello di certificato, in base al nome, a una richiesta.

Usando CertEnroll.dll, il metodo preferito per incorporare un modello in una richiesta di certificato è usare il metodo [**InitializeFromTemplateName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename) in un oggetto richiesta PKCS \# 10 o [*PKCS) o il metodo [**InitializeFromInnerRequestTemplateName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename) in una richiesta CMC.

Se un modello specifico non è disponibile nel client ma è previsto che sia compreso dall'autorità [*di*](/windows/desktop/SecGloss/c-gly) certificazione (CA), è possibile usare l'interfaccia [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) per aggiungere un modello versione 1 oppure è possibile usare l'interfaccia [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate) per aggiungere un modello versione 2 a una richiesta di certificato. Ad esempio, per aggiungere un modello versione 1, eseguire le azioni seguenti:

1.  Creare un [**oggetto IX509Extensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
2.  Creare un [**oggetto IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) e chiamare il [**metodo InitializeEncode,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensiontemplatename-initializeencode) specificando il nome del modello.
3.  Aggiungere l'estensione creata alla [**raccolta IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chiamando il [**metodo Add.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add)
4.  Creare un [**oggetto IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) e chiamare il [**metodo InitializeEncode,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) specificando la raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) nell'input.
5.  Recuperare un oggetto raccolta [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) chiamando la proprietà [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) su un oggetto richiesta [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) esistente.

## <a name="addcerttypetorequestwstrex"></a>AddCertTypeToRequestWStrEx

La [**funzione AddCertTypeToRequestWStrEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addcerttypetorequestwstrex) in Xenroll.dll aggiunge un modello di certificato a una richiesta in base al nome, all'identificatore di oggetto e alla versione.

Per informazioni su come usare CertEnroll.dll per incorporare informazioni sul modello in una richiesta, vedere AddCertTypeToRequestWStr.

## <a name="addextensionstorequest"></a>AddExtensionsToRequest

La [**funzione AddExtensionsToRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest) in Xenroll.dll aggiunge una raccolta di estensioni a una richiesta.

In CertEnroll.dll, le estensioni vengono aggiunte alla raccolta di attributi di una richiesta CMC o PKCS \# 10. Per aggiungere estensioni, eseguire le azioni seguenti:

1.  Creare un [**oggetto IX509Extensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
2.  Creare un [**oggetto IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) e chiamare il metodo [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extension-initialize) per creare un'estensione da un identificatore di oggetto e un valore di estensione oppure usare una delle interfacce elencate in precedenza per definire una delle estensioni più comuni.
3.  Aggiungere ogni nuova estensione creata nel passaggio precedente alla raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chiamando il [**metodo Add.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add)

## <a name="addextensiontorequestwstr"></a>addExtensionToRequestWStr

La [**funzione addExtensionToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addextensiontorequestwstr) in Xenroll.dll aggiunge un'estensione specifica alla richiesta.

In CertEnroll.dll, un'estensione specifica deve essere definita e aggiunta a una raccolta di estensioni prima che la raccolta di estensioni venga aggiunta alla raccolta di attributi di una richiesta CMC o PKCS \# 10. Per altre informazioni, vedere la discussione AddExtensionsToRequest precedente.

## <a name="enablesmimecapabilities"></a>EnableSMIMECapabilities

La [**funzione EnableSMIMECapabilities**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities) in Xenroll.dll specifica o recupera un valore booleano che indica se aggiungere l'estensione **SMIMECapabilities** alla richiesta.

È possibile chiamare la [**proprietà SmimeCapabilities**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities) sull'oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) per aggiungere automaticamente un oggetto [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities) alla richiesta prima della codifica.

## <a name="includesubjectkeyid"></a>IncludeSubjectKeyID

La [**funzione IncludeSubjectKeyID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_includesubjectkeyid) in Xenroll.dll specifica o recupera un valore booleano che indica se aggiungere l'estensione **SubjectKeyIdentifier** alla richiesta.

Per impostazione predefinita, **l'estensione SubjectKeyIdentifier** viene creata quando viene inizializzato l'oggetto richiesta [**IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) È possibile eseguire l'override di questo comportamento chiamando la [**proprietà SuppressOids.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids)

Se si dispone di una coppia di chiavi [*pubblica/privata,*](/windows/desktop/SecGloss/p-gly)è anche possibile usare l'interfaccia [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) in CertEnroll.dll per aggiungere **un'estensione SubjectKeyIdentifier** a una richiesta di certificato eseguendo le azioni seguenti:

1.  Creare un [**oggetto IX509Extensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
2.  Creare un [**oggetto IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) e chiamare il [**metodo InitializeEncode,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode) specificando una stringa che contiene l'identificatore. In genere, si tratta di un hash SHA-1 a 20 byte [*della*](/windows/desktop/SecGloss/p-gly) chiave pubblica contenuta nel certificato di firma della CA.
3.  Aggiungere l'estensione creata alla [**raccolta IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chiamando il [**metodo Add.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add)
4.  Creare un [**oggetto IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) e chiamare il [**metodo InitializeEncode,**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) specificando la raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) nell'input.
5.  Recuperare un oggetto raccolta [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) chiamando la proprietà [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) su un oggetto richiesta [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) esistente.

## <a name="resetextensions"></a>resetExtensions

La [**funzione resetExtensions**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetextensions) in Xenroll.dll rimuove la raccolta di estensioni dalla richiesta.

Per rimuovere un'estensione da una richiesta in base al numero di indice usando CertEnroll.dll, chiamare il [**metodo Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-remove) sulla [**raccolta IX509Extensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) Per rimuovere tutti gli attributi da una richiesta, chiamare il [**metodo Clear.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-clear)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
</dt> <dt>

[**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
</dt> </dl>

 

 
