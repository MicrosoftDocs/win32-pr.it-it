---
title: Ricerca di gruppi in base all'ambito o al tipo in un dominio
description: Nei domini di Windows 2000 è presente una singola classe denominata Group per tutti gli ambiti di gruppo (dominio locale, globale, universale) e tipi (sicurezza, distribuzione).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Ricerca di gruppi in base all'ambito o al tipo in un dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724426"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a><span data-ttu-id="fb279-104">Ricerca di gruppi in base all'ambito o al tipo in un dominio</span><span class="sxs-lookup"><span data-stu-id="fb279-104">Searching for Groups by Scope or Type in a Domain</span></span>

<span data-ttu-id="fb279-105">Nei domini di Windows 2000 è presente una singola classe denominata [**Group**](/windows/desktop/ADSchema/c-group) per tutti gli ambiti di gruppo (dominio locale, globale, universale) e tipi (sicurezza, distribuzione).</span><span class="sxs-lookup"><span data-stu-id="fb279-105">In Windows 2000 domains, there is single class called [**group**](/windows/desktop/ADSchema/c-group) for all group scopes (Domain Local, Global, Universal) and types (security, distribution).</span></span> <span data-ttu-id="fb279-106">L'attributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) dell'oggetto Group specifica il tipo e l'ambito del gruppo.</span><span class="sxs-lookup"><span data-stu-id="fb279-106">The [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute of the group object specifies the group type and scope.</span></span>

<span data-ttu-id="fb279-107">Per utilizzare il tipo o l'ambito per la ricerca di gruppi in domini Windows 2000, utilizzare un filtro che contenga una regola di corrispondenza per l'attributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="fb279-107">To use type or scope to search for groups on Windows 2000 domains, use a filter that contains a matching rule for the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="fb279-108">Per altre informazioni sulle regole di corrispondenza, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="fb279-108">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="fb279-109">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire la ricerca di gruppi in un dominio, vedere il [codice di esempio per la ricerca di gruppi in un dominio](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="fb279-109">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

## <a name="example-ldap-query-strings"></a><span data-ttu-id="fb279-110">Stringhe di query LDAP di esempio</span><span class="sxs-lookup"><span data-stu-id="fb279-110">Example LDAP Query Strings</span></span>

<span data-ttu-id="fb279-111">Negli esempi di stringhe di query seguenti viene illustrato come costruire una stringa di query LDAP utilizzata per cercare o filtrare tipi di gruppo specifici.</span><span class="sxs-lookup"><span data-stu-id="fb279-111">The following query string examples show how to construct an LDAP query string used to search for or filter specific group types.</span></span>

<span data-ttu-id="fb279-112">Nella stringa di query seguente vengono cercati i gruppi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fb279-112">The following query string will search for security groups.</span></span> <span data-ttu-id="fb279-113">Questo esempio USA "-2147483648" come equivalente decimale del flag di **\_ sicurezza del tipo di gruppo \_ \_ \_ ADS** .</span><span class="sxs-lookup"><span data-stu-id="fb279-113">This example uses "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



<span data-ttu-id="fb279-114">La stringa di query seguente cerca i gruppi di distribuzione universali; ovvero i gruppi che contengono il **tipo di gruppo ADS flag di \_ \_ \_ \_ gruppo universale** e non contengono il flag del **tipo di gruppo Ads \_ \_ \_ \_ abilitato** per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fb279-114">The following query string will search for universal distribution groups; that is, groups that contain the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** flag and do not contain the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span> <span data-ttu-id="fb279-115">In questo esempio viene usato "8" come equivalente decimale del **tipo di gruppo ADS di gruppo \_ \_ \_ universale \_** e "-2147483648" come equivalente decimale del flag per la sicurezza del **tipo di \_ gruppo \_ \_ \_ ADS** .</span><span class="sxs-lookup"><span data-stu-id="fb279-115">This example uses "8" as the decimal equivalent of **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** and "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 