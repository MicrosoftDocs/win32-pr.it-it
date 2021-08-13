---
description: In pratica, la struttura di una richiesta CMC, illustrata dalla sintassi seguente, è relativamente complessa perché spesso contiene richieste annidate.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Attributi CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b98e30c257234ebee864a1749ceecee7b79e25a9e11c9f1f190c60f3154ef64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902064"
---
# <a name="cmc-attributes"></a>Attributi CMC

In pratica, la struttura di una richiesta CMC, illustrata dalla sintassi seguente, è relativamente complessa perché spesso contiene richieste annidate. Ad esempio, una richiesta CMC può contenere zero o una richiesta PKCS 10 in una sequenza TaggedRequest e può contenere zero o un messaggio PKCS 7 in una sequenza \#  \# **TaggedContentInfo.** Ogni messaggio PKCS 7 annidato può contenere una richiesta CMC che a sua volta può \# contenere più richieste. Il numero di livelli di annidamento è teoricamente illimitato, ma l'autorità di certificazione (CA) è in genere configurata per limitare le dimensioni di una richiesta. Gli attributi possono essere applicati alla richiesta di primo livello o alle richieste annidate. Questa operazione viene illustrata nelle sezioni seguenti.

## <a name="cmcdata-structure"></a>Struttura CMCData

Una richiesta CMC contiene sequenze di **strutture ASN.1,** **TaggedRequest** e **TaggedContentInfo.**

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

## <a name="taggedattribute-structure"></a>Struttura TaggedAttribute

Gli attributi vengono inclusi in una richiesta di certificato CMC aggiungendoli alla raccolta **TaggedAttribute.** Ogni struttura nella raccolta contiene un ID intero, un identificatore di oggetto ASN.1 (OID) e un set di valori. I valori possibili possono essere uno dei seguenti.

``` syntax
CmcAddAttributes ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   attributes              Attributes
}

Attributes ::= SET OF Attribute
Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

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

SenderNonce ::= OCTET STRING

TransactID ::= OCTET STRING

RegInfo ::= OCTET STRING
```

## <a name="cmcaddattributes"></a>CMCAddAttributes

Se gli attributi in questa struttura si applicano a una richiesta PKCS 10 annidata, il campo \# **certReferences** conterrà **bodyPartID** che identifica la richiesta. Se gli attributi si applicano a una richiesta CMC annidata, il campo **pkiDataReference** conterrà **bodyPartID** della richiesta. Attualmente, solo uno di questi campi può essere diverso da zero. Gli attributi che è possibile includere sono elencati [nell'argomento Attributi](supported-attributes.md) supportati.

## <a name="cmcaddextensions"></a>CmcAddExtensions

Questa struttura può contenere estensioni X.509 versione 3 e estensioni definite da Microsoft. Questo attributo viene definito tramite [**l'interfaccia IX509AttributeExtensions.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) Se le estensioni si applicano a una richiesta PKCS 10 annidata, il campo \# **certReferences** conterrà **bodyPartID** che identifica la richiesta. Se le estensioni si applicano a una richiesta CMC annidata, il campo **pkiDataReference** conterrà **bodyPartID** della richiesta. Attualmente, solo uno di questi campi può essere diverso da zero.

## <a name="sendernonce"></a>SenderNonce

Un nonce è un dato binario casuale o pseudo-casuale che può essere incluso in una transazione di richiesta e risposta del certificato per garantire che la risposta o la richiesta non sia una ripetizione di un messaggio precedente. Per altre informazioni, vedere la [**proprietà SenderNonce.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce)

## <a name="transactid"></a>TransactID

Una round trip richiesta di certificato e una transazione di risposta possono essere rilevate usando un identificatore. Il client genera un ID transazione e lo conserva fino a quando il certificato o l'autorità di registrazione non risponde con un messaggio che completa la transazione. La risposta include l'identificatore. Per altre informazioni, vedere la [**proprietà TransactionId.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid)

## <a name="reginfo"></a>RegInfo

Questo attributo può essere usato per contenere le informazioni di registrazione che il client sceglie di inserire nella richiesta CMC. Il valore dell'attributo è una stringa che contiene coppie nome-valore concatenate. Per altre informazioni, vedere la [**proprietà NameValuePairs.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi supportati](supported-attributes.md)
</dt> </dl>

 

 



