---
description: Le estensioni vengono incluse in una richiesta CMC aggiungendole alla struttura TaggedAttributes illustrata nell'esempio di sintassi ASN.1 seguente. Per altre informazioni, vedere l'argomento Attributi.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Estensioni CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d29873bc43f7a7229b363a7b09cdf03a23127cc5d5e0e738036c6005a6cc7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901844"
---
# <a name="cmc-extensions"></a>Estensioni CMC

Le estensioni vengono incluse in una richiesta CMC aggiungendole alla struttura **TaggedAttributes** illustrata nell'esempio di sintassi ASN.1 seguente. Per altre informazioni, vedere [l'argomento](attributes.md) Attributi.

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

Ogni struttura nella **raccolta TaggedAttributes** contiene un ID integer, un identificatore di oggetto ASN.1 (OID) e un set di valori. Le estensioni vengono incorporate in una richiesta aggiungendo una **struttura CmcAddExtensions** al **campo values.** La sintassi della struttura ASN.1 è illustrata nell'esempio seguente. L'identificatore di oggetto è **XCN \_ OID \_ CMC \_ ADD \_ EXTENSIONS** (1.3.6.1.5.5.7.7.8).

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

La procedura seguente illustra come usare l'API di registrazione certificati per aggiungere estensioni a una richiesta di certificato CMC.

**Per usare l'API di registrazione certificati per aggiungere estensioni a una richiesta di certificato CMC**

1.  Creare un'estensione usando una delle interfacce disponibili che derivano dall'interfaccia [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) o usare direttamente l'oggetto **IX509Extension** per creare estensioni personalizzate.
2.  Chiamare la [**proprietà X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) sull'oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) per recuperare una [**raccolta IX509Extensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
3.  Aggiungere le estensioni create nel passaggio 1 alla [**raccolta IX509Extensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
4.  Chiamare [**Enroll per**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) eseguire automaticamente le azioni seguenti:
    -   Recuperare un [**oggetto ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) dall'oggetto [**IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
    -   Creare e inizializzare [**un oggetto IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) usando la raccolta [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperata nel passaggio 2.
    -   Creare una [**raccolta IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) e aggiungerne l'oggetto [**IX509AttributeExtensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
    -   Usare la [**raccolta IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) per inizializzare un [**oggetto ICryptAttribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
    -   Aggiungere [**l'oggetto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) alla [**raccolta ICryptAttributes.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributes (Attributi)](attributes.md)
</dt> <dt>

[Architettura degli attributi](attribute-architecture.md)
</dt> <dt>

[Attributi CMC](cmc-attributes.md)
</dt> <dt>

[Estensioni](extensions.md)
</dt> </dl>

 

 



