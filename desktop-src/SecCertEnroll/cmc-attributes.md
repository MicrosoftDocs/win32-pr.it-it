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
# <a name="cmc-attributes"></a><span data-ttu-id="32535-103">Attributi CMC</span><span class="sxs-lookup"><span data-stu-id="32535-103">CMC Attributes</span></span>

<span data-ttu-id="32535-104">In pratica, la struttura di una richiesta CMC, mostrata dalla sintassi seguente, è relativamente complessa perché contiene spesso richieste nidificate.</span><span class="sxs-lookup"><span data-stu-id="32535-104">In practice, the structure of a CMC request, shown by the following syntax, is relatively complex because it often contains nested requests.</span></span> <span data-ttu-id="32535-105">Una richiesta CMC, ad esempio, può contenere una o più \# richieste PKCS 10 in una sequenza **TaggedRequest** e può contenere zero o un messaggio PKCS \# 7 in una sequenza **TaggedContentInfo** .</span><span class="sxs-lookup"><span data-stu-id="32535-105">For example, a CMC request can contain zero or one PKCS \#10 requests in a **TaggedRequest** sequence, and it can contain zero or one PKCS \#7 messages in a **TaggedContentInfo** sequence.</span></span> <span data-ttu-id="32535-106">Ogni messaggio PKCS \# 7 annidato può contenere una richiesta CMC che può, a sua volta, contenere più richieste.</span><span class="sxs-lookup"><span data-stu-id="32535-106">Each nested PKCS \#7 message can contain a CMC request which can, in turn, contain more requests.</span></span> <span data-ttu-id="32535-107">Il numero di livelli di nidificazione è teoricamente illimitato, ma l'autorità di certificazione (CA) viene in genere configurata per limitare le dimensioni di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="32535-107">The number of nesting levels is theoretically unlimited, but the certification authority (CA) is typically configured to limit the size of a request.</span></span> <span data-ttu-id="32535-108">Gli attributi possono essere applicati alla richiesta di primo livello o alle richieste nidificate.</span><span class="sxs-lookup"><span data-stu-id="32535-108">Attributes can be applied to the top level request or to the nested requests.</span></span> <span data-ttu-id="32535-109">Questo argomento viene descritto nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="32535-109">This is discussed in the following sections.</span></span>

## <a name="cmcdata-structure"></a><span data-ttu-id="32535-110">Struttura CMCData</span><span class="sxs-lookup"><span data-stu-id="32535-110">CMCData Structure</span></span>

<span data-ttu-id="32535-111">Una richiesta CMC contiene sequenze di strutture **TaggedAttribute**, **TaggedRequest** e **TaggedContentInfo** ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="32535-111">A CMC request contains sequences of **TaggedAttribute**, **TaggedRequest**, and **TaggedContentInfo** ASN.1 structures.</span></span>

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

## <a name="taggedattribute-structure"></a><span data-ttu-id="32535-112">Struttura TaggedAttribute</span><span class="sxs-lookup"><span data-stu-id="32535-112">TaggedAttribute Structure</span></span>

<span data-ttu-id="32535-113">Gli attributi sono inclusi in una richiesta di certificato CMC aggiungendoli alla raccolta **TaggedAttribute** .</span><span class="sxs-lookup"><span data-stu-id="32535-113">Attributes are included in a CMC certificate request by adding them to the **TaggedAttribute** collection.</span></span> <span data-ttu-id="32535-114">Ogni struttura della raccolta contiene un ID di tipo Integer, un identificatore di oggetto ASN. 1 (OID) e un set di valori.</span><span class="sxs-lookup"><span data-stu-id="32535-114">Each structure in the collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="32535-115">I possibili valori sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="32535-115">The possible values can be any of the following.</span></span>

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

## <a name="cmcaddattributes"></a><span data-ttu-id="32535-116">CMCAddAttributes</span><span class="sxs-lookup"><span data-stu-id="32535-116">CMCAddAttributes</span></span>

<span data-ttu-id="32535-117">Se gli attributi in questa struttura si applicano a una \# richiesta PKCS 10 annidata, il campo **certReferences** conterrà il **BodyPartID** che identifica la richiesta.</span><span class="sxs-lookup"><span data-stu-id="32535-117">If the attributes in this structure apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="32535-118">Se gli attributi si applicano a una richiesta CMC annidata, il campo **pkiDataReference** conterrà il **BodyPartID** della richiesta.</span><span class="sxs-lookup"><span data-stu-id="32535-118">If the attributes apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="32535-119">Attualmente, solo uno di questi campi può essere diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="32535-119">Currently, only one of these fields can be nonzero.</span></span> <span data-ttu-id="32535-120">Gli attributi che possono essere inclusi sono elencati nell'argomento [attributi supportati](supported-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="32535-120">The attributes that can be included are listed in the [Supported Attributes](supported-attributes.md) topic.</span></span>

## <a name="cmcaddextensions"></a><span data-ttu-id="32535-121">CmcAddExtensions</span><span class="sxs-lookup"><span data-stu-id="32535-121">CmcAddExtensions</span></span>

<span data-ttu-id="32535-122">Questa struttura può contenere le estensioni X. 509 versione 3 e le estensioni definite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32535-122">This structure can contain X.509 version 3 extensions plus extensions defined by Microsoft.</span></span> <span data-ttu-id="32535-123">Questo attributo viene definito tramite l'interfaccia [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="32535-123">This attribute is defined by using the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface.</span></span> <span data-ttu-id="32535-124">Se le estensioni si applicano a una \# richiesta PKCS 10 annidata, il campo **certReferences** conterrà il **BodyPartID** che identifica la richiesta.</span><span class="sxs-lookup"><span data-stu-id="32535-124">If the extensions apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="32535-125">Se le estensioni si applicano a una richiesta CMC annidata, il campo **pkiDataReference** conterrà il **BodyPartID** della richiesta.</span><span class="sxs-lookup"><span data-stu-id="32535-125">If the extensions apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="32535-126">Attualmente, solo uno di questi campi può essere diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="32535-126">Currently, only one of these fields can be nonzero.</span></span>

## <a name="sendernonce"></a><span data-ttu-id="32535-127">SenderNonce</span><span class="sxs-lookup"><span data-stu-id="32535-127">SenderNonce</span></span>

<span data-ttu-id="32535-128">Un parametro nonce è costituito da dati binari casuali o pseudo-casuali che possono essere inclusi in una richiesta di certificato e una transazione di risposta per garantire che la risposta o la richiesta non sia una ripetizione di un messaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="32535-128">A nonce is random or pseudo-random binary data that can be included in a certificate request and response transaction to help ensure that the response or request is not a repeat of a previous message.</span></span> <span data-ttu-id="32535-129">Per ulteriori informazioni, vedere la proprietà [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .</span><span class="sxs-lookup"><span data-stu-id="32535-129">For more information, see the [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) property.</span></span>

## <a name="transactid"></a><span data-ttu-id="32535-130">TransactID</span><span class="sxs-lookup"><span data-stu-id="32535-130">TransactID</span></span>

<span data-ttu-id="32535-131">È possibile tenere traccia di una richiesta di certificato round trip e di una transazione di risposta usando un identificatore.</span><span class="sxs-lookup"><span data-stu-id="32535-131">A round trip certificate request and response transaction can be tracked using an identifier.</span></span> <span data-ttu-id="32535-132">Il client genera un ID transazione e lo mantiene fino a quando il certificato o l'autorità di registrazione non risponde con un messaggio che completa la transazione.</span><span class="sxs-lookup"><span data-stu-id="32535-132">The client generates a transaction ID and retains it until the certificate or registration authority responds with a message that completes the transaction.</span></span> <span data-ttu-id="32535-133">La risposta include l'identificatore.</span><span class="sxs-lookup"><span data-stu-id="32535-133">The response includes the identifier.</span></span> <span data-ttu-id="32535-134">Per ulteriori informazioni, vedere la proprietà [**ID transazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .</span><span class="sxs-lookup"><span data-stu-id="32535-134">For more information, see the [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) property.</span></span>

## <a name="reginfo"></a><span data-ttu-id="32535-135">RegInfo</span><span class="sxs-lookup"><span data-stu-id="32535-135">RegInfo</span></span>

<span data-ttu-id="32535-136">Questo attributo può essere usato per contenere le informazioni di registrazione che il client sceglie di inserire nella richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="32535-136">This attribute can be used to contain any registration information that the client chooses to put into the CMC request.</span></span> <span data-ttu-id="32535-137">Il valore dell'attributo è una stringa che contiene coppie nome-valore concatenate.</span><span class="sxs-lookup"><span data-stu-id="32535-137">The attribute value is string that contains concatenated name-value pairs.</span></span> <span data-ttu-id="32535-138">Per ulteriori informazioni, vedere la proprietà [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .</span><span class="sxs-lookup"><span data-stu-id="32535-138">For more information, see the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32535-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32535-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32535-140">Attributi supportati</span><span class="sxs-lookup"><span data-stu-id="32535-140">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



