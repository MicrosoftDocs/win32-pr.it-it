---
description: Gli attributi possono essere aggiunti a una richiesta di certificato per fornire a un'autorità di certificazione (CA) informazioni aggiuntive che può usare durante la creazione e il rilascio di un certificato.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Funzioni degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a353b5beb5b7da048edf8712c5d82545fd326a7d1720748705ae093aaa2cc44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903113"
---
# <a name="attribute-functions"></a>Funzioni degli attributi

Gli attributi possono essere aggiunti a una richiesta di certificato per fornire [*a*](/windows/desktop/SecGloss/c-gly) un'autorità di certificazione (CA) informazioni aggiuntive che può usare durante la creazione e il rilascio di un certificato.

CertEnroll.dll implementa le interfacce seguenti per definire gli attributi e le raccolte di attributi:

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

Le sezioni seguenti identificano le funzioni esportate da Xenroll.dll per associare gli attributi di crittografia alle richieste di certificato e illustrano come usare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie:

-   [addAttributeToRequestWStr](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [addNameValuePairToRequestWStr](#addnamevaluepairtorequestwstr)
-   [AddNameValuePairToSignatureWStr](#addnamevaluepairtosignaturewstr)
-   [Clientid](#clientid)
-   [RenewalCertificate](#renewalcertificate)
-   [resetAttributes](#resetattributes)
-   [Argomenti correlati](#related-topics)

## <a name="addattributetorequestwstr"></a>addAttributeToRequestWStr

La [**funzione addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) in Xenroll.dll aggiunge un attributo a una richiesta di certificato.

In generale, per aggiungere un attributo a una richiesta usando gli oggetti implementati in CertEnroll.dll, è possibile eseguire le azioni seguenti:

1.  Creare un [**oggetto raccolta IX509Attributes.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
2.  Creare un [**oggetto IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) e chiamare il metodo [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) per creare un attributo da un identificatore di oggetto e da un valore di attributo oppure usare una delle interfacce elencate in precedenza per definire uno degli attributi più comuni.
3.  Aggiungere ogni nuovo attributo creato nel passaggio precedente alla raccolta [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) usando il [**metodo Add.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add)
4.  Creare un [**oggetto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) e inizializzarlo chiamando il [**metodo InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) e specificando la raccolta [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) nell'input.
5.  Recuperare un oggetto raccolta [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) chiamando la proprietà [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) su un oggetto richiesta [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) esistente.
6.  Aggiungere [**l'oggetto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) alla [**raccolta ICryptAttributes.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

Gli attributi autenticati sono coppie nome-valore firmate da e aggiunte a una firma. La [**funzione AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) in Xenroll.dll aggiunge una matrice di attributi autenticati a una richiesta [*PKCS \# 7.*](/windows/desktop/SecGloss/p-gly)

Come illustrato in precedenza per la funzione [**addAttributeToRequestWStr,**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) è possibile usare CertEnroll.dll per definire e aggiungere facilmente una raccolta di attributi a una richiesta di certificato. Non è tuttavia possibile scegliere se l'attributo è autenticato. Il processo di registrazione prende automaticamente questa decisione.

## <a name="addnamevaluepairtorequestwstr"></a>addNameValuePairToRequestWStr

La [**funzione addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) in Xenroll.dll aggiunge una coppia nome-valore non autenticata a una richiesta.

È possibile usare l'interfaccia [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) in CertEnroll.dll per definire una coppia nome-valore ed è possibile aggiungere una raccolta di coppie nome-valore a un oggetto richiesta CMC eseguendo le azioni seguenti:

1.  Creare e inizializzare un [**oggetto IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) Il processo di inizializzazione crea una [**raccolta IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) vuota.
2.  Chiamare la [**proprietà NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) su un oggetto richiesta CMC esistente per recuperare la raccolta.
3.  Creare e inizializzare un [**oggetto IX509NameValuePair.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
4.  Aggiungere ogni nuova coppia nome-valore alla raccolta [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) chiamando il [**metodo Add.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add)

Il processo di registrazione inserisce la raccolta di coppie nome-valore nella **struttura TaggedAttribute** della richiesta CMC.

## <a name="addnamevaluepairtosignaturewstr"></a>AddNameValuePairToSignatureWStr

La [**funzione AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) in Xenroll.dll aggiunge una coppia nome-valore autenticata a una richiesta. Viene in genere usato per specificare il nome del richiedente in una richiesta enroll-on-behalf-of (EOBO).

In CertEnroll.dll usare la [**proprietà RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) per specificare il nome in una richiesta EOBO.

## <a name="clientid"></a>ClientId

La [**funzione ClientId**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) in Xenroll.dll specifica o recupera un **attributo ClientId.**

Usare la [**proprietà ClientId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) in CertEnroll.dll aggiungere questo attributo a una richiesta CMC o PKCS \# 10.

## <a name="renewalcertificate"></a>RenewalCertificate

La [**funzione RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) in Xenroll.dll specifica o recupera un **attributo RenewalCertificate.**

In CertEnroll.dll, quando si chiama [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) su un oggetto PKCS 7 o \# PKCS , viene creato automaticamente.

## <a name="resetattributes"></a>resetAttributes

La [**funzione resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) in Xenroll.dll rimuove la raccolta di attributi da una richiesta.

Per rimuovere un attributo da una richiesta in base all'indice usando CertEnroll.dll, chiamare il [**metodo Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) sulla [**raccolta IX509Attributes.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) Per rimuovere tutti gli attributi da una richiesta, chiamare il [**metodo Clear.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
