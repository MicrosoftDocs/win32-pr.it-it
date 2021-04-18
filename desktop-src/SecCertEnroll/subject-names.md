---
description: Il campo oggetto di una \# richiesta di certificato PKCS 10 contiene il nome distinto dell'entità che richiede il certificato.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Nomi soggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314140"
---
# <a name="subject-names"></a>Nomi soggetto

Il campo **oggetto** di una \# richiesta di certificato PKCS 10 contiene il nome distinto dell'entità che richiede il certificato.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

Il nome distinto è costituito da una sequenza di nomi distinti relativi (RDNs). Ogni RDN è costituito da un set di attributi e ogni attributo è costituito da un identificatore di oggetto e da un valore. Il tipo di dati del valore è identificato dalla struttura **DirectoryString** .

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

 

 
