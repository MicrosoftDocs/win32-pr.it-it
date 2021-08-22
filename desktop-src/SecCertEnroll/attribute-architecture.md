---
description: Usato per aggiungere attributi a una richiesta di certificato.
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: Architettura degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d09a2a351635547c21357477290cb3335cb8c1da042d680762140b48b03f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903238"
---
# <a name="attribute-architecture"></a>Architettura degli attributi

Le interfacce seguenti vengono usate per aggiungere attributi a una richiesta di certificato:

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

L'architettura segue quella definita nel modulo ASN.1 della sintassi della richiesta di certificazione PKCS \# 10.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

La [**raccolta ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) corrisponde al campo **attributes** e ogni [**oggetto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) nella raccolta corrisponde a una struttura **Attribute** ASN.1.

Ogni **attributo** è costituito da un identificatore di oggetto (OID) e da zero o più valori associati all'OID. Una singola coppia OID-valore è rappresentata da [**un'interfaccia IX509Attribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) È possibile usare una raccolta [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) per inizializzare un [**oggetto ICryptAttribute,**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) ma ogni attributo nella raccolta deve essere associato allo stesso OID. In genere, un attributo ha un solo valore.

È possibile usare una delle interfacce seguenti, che derivano da [**IX509Attribute,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)per creare una singola coppia di attributi OID/valore:

-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

Ad esempio, la procedura seguente illustra come creare un **attributo ClientId.**

**Per creare un **attributo ClientId****

1.  Recuperare un [**oggetto ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) da [**un oggetto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) o [**IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
2.  Creare e inizializzare un [**oggetto IX509AttributeClientId.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
3.  Creare una [**raccolta IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) e aggiungere [**l'oggetto IX509AttributeClientId.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
4.  Usare la [**raccolta IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) per inizializzare un [**oggetto ICryptAttribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
5.  Aggiungere [**l'oggetto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) alla raccolta recuperata nel passaggio 1.

L'esempio seguente illustra l'output ASN.1 **dell'attributo ClientId.** L'attributo contiene il nome DNS del computer in cui è stata generata la richiesta (test3d.jdomcsc.nttest.microsoft.com), il nome SAM dell'utente (amministratore JDOMCSC) e il nome dell'applicazione che ha generato la richiesta \\ (certreq).

``` syntax
0136: 30 57; SEQUENCE (57 Bytes)
0138: |  06 09                            ; OBJECT_ID (9 Bytes)
013a: |  |  2b 06 01 04 01 82 37 15  14
      |  |     ; 1.3.6.1.4.1.311.21.20 Client Information
0143: |  |  31 4a                         ; SET (4a Bytes)
0145: |  |     30 48                      ; SEQUENCE (48 Bytes)
0147: |  |        02 01                   ; INTEGER (1 Bytes)
0149: |  |        |  09
014a: |  |        0c 23                   ; UTF8_STRING (23 Bytes)
014c: |  |        |  74 65 73 74 33 64 2e 6a  64 6f 6d 63 73 63 2e 6e 
015c: |  |        |  74 74 65 73 74 2e 6d 69  63 72 6f 73 6f 66 74 2e 
016c: |  |        |  63 6f 6d                                         
      |  |        |     ; "test3d.jdomcsc.nttest.microsoft.com"
016f: |  |        0c 15                   ; UTF8_STRING (15 Bytes)
0171: |  |        |  4a 44 4f 4d 43 53 43 5c  61 64 6d 69 6e 69 73 74 
0181: |  |        |  72 61 74 6f 72                                   
      |  |        |     ; "JDOMCSC\administrator"
0186: |  |        0c 07                   ; UTF8_STRING (7 Bytes)
0188: |  |           63 65 72 74 72 65 71                             
      |  |              ; "certreq"
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



