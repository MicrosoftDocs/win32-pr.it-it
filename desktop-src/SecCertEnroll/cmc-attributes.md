---
description: In pratica, la struttura di una richiesta CMC, mostrata dalla sintassi seguente, è relativamente complessa perché contiene spesso richieste nidificate.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Attributi CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6778575a9359ad5b8764528fb0351b68efc1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758072"
---
# <a name="cmc-attributes"></a>Attributi CMC

In pratica, la struttura di una richiesta CMC, mostrata dalla sintassi seguente, è relativamente complessa perché contiene spesso richieste nidificate. Una richiesta CMC, ad esempio, può contenere una o più \# richieste PKCS 10 in una sequenza **TaggedRequest** e può contenere zero o un messaggio PKCS \# 7 in una sequenza **TaggedContentInfo** . Ogni messaggio PKCS \# 7 annidato può contenere una richiesta CMC che può, a sua volta, contenere più richieste. Il numero di livelli di nidificazione è teoricamente illimitato, ma l'autorità di certificazione (CA) viene in genere configurata per limitare le dimensioni di una richiesta. Gli attributi possono essere applicati alla richiesta di primo livello o alle richieste nidificate. Questo argomento viene descritto nelle sezioni seguenti.

## <a name="cmcdata-structure"></a>Struttura CMCData

Una richiesta CMC contiene sequenze di strutture **TaggedAttribute**, **TaggedRequest** e **TaggedContentInfo** ASN. 1.

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

Gli attributi sono inclusi in una richiesta di certificato CMC aggiungendoli alla raccolta **TaggedAttribute** . Ogni struttura della raccolta contiene un ID di tipo Integer, un identificatore di oggetto ASN. 1 (OID) e un set di valori. I possibili valori sono i seguenti.

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

Se gli attributi in questa struttura si applicano a una \# richiesta PKCS 10 annidata, il campo **certReferences** conterrà il **BodyPartID** che identifica la richiesta. Se gli attributi si applicano a una richiesta CMC annidata, il campo **pkiDataReference** conterrà il **BodyPartID** della richiesta. Attualmente, solo uno di questi campi può essere diverso da zero. Gli attributi che possono essere inclusi sono elencati nell'argomento [attributi supportati](supported-attributes.md) .

## <a name="cmcaddextensions"></a>CmcAddExtensions

Questa struttura può contenere le estensioni X. 509 versione 3 e le estensioni definite da Microsoft. Questo attributo viene definito tramite l'interfaccia [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Se le estensioni si applicano a una \# richiesta PKCS 10 annidata, il campo **certReferences** conterrà il **BodyPartID** che identifica la richiesta. Se le estensioni si applicano a una richiesta CMC annidata, il campo **pkiDataReference** conterrà il **BodyPartID** della richiesta. Attualmente, solo uno di questi campi può essere diverso da zero.

## <a name="sendernonce"></a>SenderNonce

Un parametro nonce è costituito da dati binari casuali o pseudo-casuali che possono essere inclusi in una richiesta di certificato e una transazione di risposta per garantire che la risposta o la richiesta non sia una ripetizione di un messaggio precedente. Per ulteriori informazioni, vedere la proprietà [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .

## <a name="transactid"></a>TransactID

È possibile tenere traccia di una richiesta di certificato round trip e di una transazione di risposta usando un identificatore. Il client genera un ID transazione e lo mantiene fino a quando il certificato o l'autorità di registrazione non risponde con un messaggio che completa la transazione. La risposta include l'identificatore. Per ulteriori informazioni, vedere la proprietà [**ID transazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .

## <a name="reginfo"></a>RegInfo

Questo attributo può essere usato per contenere le informazioni di registrazione che il client sceglie di inserire nella richiesta CMC. Il valore dell'attributo è una stringa che contiene coppie nome-valore concatenate. Per ulteriori informazioni, vedere la proprietà [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi supportati](supported-attributes.md)
</dt> </dl>

 

 



