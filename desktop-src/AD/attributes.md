---
title: Attributi (AD DS)
description: Ogni oggetto in Active Directory Domain Services contiene un set di attributi che definiscono le caratteristiche dell'oggetto.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- attributi AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046558"
---
# <a name="attributes-ad-ds"></a><span data-ttu-id="9e905-104">Attributi (AD DS)</span><span class="sxs-lookup"><span data-stu-id="9e905-104">Attributes (AD DS)</span></span>

<span data-ttu-id="9e905-105">Ogni oggetto in Active Directory Domain Services contiene un set di attributi che definiscono le caratteristiche dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e905-105">Each object in Active Directory Domain Services contains a set of attributes that define the characteristics of the object.</span></span> <span data-ttu-id="9e905-106">Ogni attributo è descritto da un oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) nel contenitore dello schema che definisce l'attributo.</span><span class="sxs-lookup"><span data-stu-id="9e905-106">Each attribute is described by an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object in the schema container that defines the attribute.</span></span> <span data-ttu-id="9e905-107">La definizione dell'attributo include una varietà di dati, ad esempio i tipi di oggetto a cui si applica l'attributo e il tipo di sintassi dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="9e905-107">The attribute definition includes a variety of data, for example, what object types that the attribute applies to and the syntax type of the attribute.</span></span> <span data-ttu-id="9e905-108">Per ulteriori informazioni sulle definizioni dello schema degli attributi, vedere [caratteristiche degli attributi](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9e905-108">For more information about attribute schema definitions, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

<span data-ttu-id="9e905-109">Nell'elenco seguente sono elencati i tipi di attributi archiviati in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9e905-109">The following list lists the type of attributes that are stored in Active Directory Domain Services.</span></span>

<dl> <dt>

<span data-ttu-id="9e905-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Attributi archiviati con replica di dominio</span><span class="sxs-lookup"><span data-stu-id="9e905-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Domain-replicated, stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="9e905-111">Alcuni attributi vengono archiviati nella directory, ad esempio [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), e replicati in tutti i controller di dominio di un dominio.</span><span class="sxs-lookup"><span data-stu-id="9e905-111">Some attributes are stored in the directory (such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) and replicated to all domain controllers in a domain.</span></span> <span data-ttu-id="9e905-112">Un subset di questi attributi viene inoltre replicato nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="9e905-112">A subset of these attributes is also replicated to the global catalog.</span></span> <span data-ttu-id="9e905-113">Se si enumerano gli attributi di un oggetto dal catalogo globale, vengono restituiti solo gli attributi replicati nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="9e905-113">If you enumerate attributes of an object from the global catalog, only the attributes replicated to the global catalog are returned.</span></span> <span data-ttu-id="9e905-114">Alcuni attributi vengono indicizzati anche perché l'inclusione di una proprietà indicizzata in una query migliora le prestazioni di esecuzione delle query.</span><span class="sxs-lookup"><span data-stu-id="9e905-114">Some attributes are also indexed because including an indexed property in a query improves the query performance.</span></span>

</dd> <dt>

<span data-ttu-id="9e905-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Attributi archiviati localmente non replicati</span><span class="sxs-lookup"><span data-stu-id="9e905-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Non-replicated, locally stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="9e905-116">Gli attributi non replicati, ad esempio [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon)e [**Last-disconnessione**](/windows/desktop/ADSchema/a-lastlogoff) , vengono archiviati in ogni controller di dominio, ma non vengono replicati.</span><span class="sxs-lookup"><span data-stu-id="9e905-116">Non-replicated attributes, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon), and [**Last-Logoff**](/windows/desktop/ADSchema/a-lastlogoff) are stored on each domain controller, but are not replicated.</span></span> <span data-ttu-id="9e905-117">Gli attributi non replicati sono attributi che riguardano un particolare controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="9e905-117">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="9e905-118">Ad esempio, l'attributo **Last-Logon** è l'ultima data e ora in cui l'accesso alla rete dell'utente è stato convalidato da quel particolare controller di dominio che ha restituito la proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e905-118">For example, **Last-Logon** attribute is the last date and time that the user's network logon was validated by that particular domain controller that returned the property.</span></span> <span data-ttu-id="9e905-119">Questi attributi possono essere recuperati nello stesso modo degli attributi a livello di dominio descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9e905-119">These attributes can be retrieved in the same way as the domain-wide attributes described previously.</span></span> <span data-ttu-id="9e905-120">Tuttavia, per questi attributi, ogni controller di dominio archivia solo i valori che riguardano quel particolare controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="9e905-120">However, for these attributes, each domain controller stores only values that pertain to that particular domain controller.</span></span> <span data-ttu-id="9e905-121">Ad esempio, per ottenere l'ultima volta in cui un utente ha effettuato l'accesso al dominio, recuperare l'attributo **Last-Logon** per l'utente da ogni controller di dominio nel dominio e individuare la data e l'ora più recenti.</span><span class="sxs-lookup"><span data-stu-id="9e905-121">For example, to obtain the last time that a user logged on to the domain, retrieve the **Last-Logon** attribute for the user from every domain controller in the domain and find that latest date and time.</span></span>

</dd> <dt>

<span data-ttu-id="9e905-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Attributi non archiviati e costruiti</span><span class="sxs-lookup"><span data-stu-id="9e905-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Non-stored, constructed attributes</span></span>
</dt> <dd>

<span data-ttu-id="9e905-123">Un oggetto utente dispone inoltre di attributi costruiti che non sono archiviati nella directory, ma vengono calcolati dal controller di dominio, ad esempio [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname) e [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).</span><span class="sxs-lookup"><span data-stu-id="9e905-123">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) and [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).</span></span>

</dd> </dl>

 

 