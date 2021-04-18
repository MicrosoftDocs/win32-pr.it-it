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
# <a name="subject-names"></a><span data-ttu-id="4eb11-103">Nomi soggetto</span><span class="sxs-lookup"><span data-stu-id="4eb11-103">Subject Names</span></span>

<span data-ttu-id="4eb11-104">Il campo **oggetto** di una \# richiesta di certificato PKCS 10 contiene il nome distinto dell'entità che richiede il certificato.</span><span class="sxs-lookup"><span data-stu-id="4eb11-104">The **subject** field of a PKCS \#10 certificate request contains the distinguished name of the entity requesting the certificate.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

<span data-ttu-id="4eb11-105">Il nome distinto è costituito da una sequenza di nomi distinti relativi (RDNs).</span><span class="sxs-lookup"><span data-stu-id="4eb11-105">The distinguished name consists of a sequence of relative distinguished names (RDNs).</span></span> <span data-ttu-id="4eb11-106">Ogni RDN è costituito da un set di attributi e ogni attributo è costituito da un identificatore di oggetto e da un valore.</span><span class="sxs-lookup"><span data-stu-id="4eb11-106">Each RDN consists of a set of attributes, and each attribute consists of an object identifier and a value.</span></span> <span data-ttu-id="4eb11-107">Il tipo di dati del valore è identificato dalla struttura **DirectoryString** .</span><span class="sxs-lookup"><span data-stu-id="4eb11-107">The data type of the value is identified by the **DirectoryString** structure.</span></span>

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

<span data-ttu-id="4eb11-108">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="4eb11-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="4eb11-109">Creazione di un nome soggetto</span><span class="sxs-lookup"><span data-stu-id="4eb11-109">Creating a Subject Name</span></span>](creating-a-subject-name.md)
-   [<span data-ttu-id="4eb11-110">Codifica di un nome soggetto</span><span class="sxs-lookup"><span data-stu-id="4eb11-110">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)

## <a name="related-topics"></a><span data-ttu-id="4eb11-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4eb11-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eb11-112">Richieste</span><span class="sxs-lookup"><span data-stu-id="4eb11-112">Requests</span></span>](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
