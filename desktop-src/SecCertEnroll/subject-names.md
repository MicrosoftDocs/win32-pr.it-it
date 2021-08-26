---
description: Il campo oggetto di una richiesta di certificato PKCS \# 10 contiene il nome distinto dell'entità che richiede il certificato.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Nomi soggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be70af23c524e71c1a9b22f43e391e4f5c8302fba70f24fba1f8268ebfda6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101101"
---
# <a name="subject-names"></a>Nomi soggetto

Il **campo** oggetto di una richiesta di certificato PKCS \# 10 contiene il nome distinto dell'entità che richiede il certificato.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

Il nome distinto è costituito da una sequenza di nomi distinti relativi (RDN). Ogni RDN è costituito da un set di attributi e ogni attributo è costituito da un identificatore di oggetto e da un valore. Il tipo di dati del valore è identificato dalla **struttura DirectoryString.**

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

Per altre informazioni, vedere i seguenti argomenti:

-   [Creazione di un nome soggetto](creating-a-subject-name.md)
-   [Codifica di un nome soggetto](encoding-a-subject-name.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richieste](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
