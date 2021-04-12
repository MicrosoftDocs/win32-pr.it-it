---
title: Esecuzione di query per gli oggetti dello schema Category 1 o 2
description: L'attributo systemFlags degli oggetti attributeSchema e classSchema è una maschera di tipo integer che contiene flag che indicano le qualità di sistema aggiuntive dell'attributo o della classe.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Esecuzione di query per la categoria 1 o 2 oggetti dello schema AD
- oggetto AD, esecuzione di query per gli oggetti dello schema di categoria 1 o 2
- ANNUNCIO dello schema, esecuzione di query per gli oggetti dello schema di categoria 1 o 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336790"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a><span data-ttu-id="c4407-106">Esecuzione di query per gli oggetti dello schema Category 1 o 2</span><span class="sxs-lookup"><span data-stu-id="c4407-106">Querying for Category 1 or 2 Schema Objects</span></span>

<span data-ttu-id="c4407-107">L'attributo **systemFlags** degli oggetti **attributeSchema** e **classSchema** è una maschera di tipo integer che contiene flag che indicano le qualità di sistema aggiuntive dell'attributo o della classe.</span><span class="sxs-lookup"><span data-stu-id="c4407-107">The **systemFlags** attribute of **attributeSchema** and **classSchema** objects is an integer bitmask that contains flags that indicate additional system qualities of the attribute or class.</span></span> <span data-ttu-id="c4407-108">L'enumerazione [**Ads \_ SYSTEMFLAG \_ enum**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contiene valori che corrispondono ai bit che è possibile impostare nell'attributo **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="c4407-108">The [**ADS\_SYSTEMFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) enumeration contains values that correspond to the bits you can set in the **systemFlags** attribute.</span></span> <span data-ttu-id="c4407-109">Sono presenti altri bit **systemFlags** che non è possibile impostare, ad esempio il bit 0x10 che indica se l'attributo o la classe è la categoria 1 o la categoria 2.</span><span class="sxs-lookup"><span data-stu-id="c4407-109">There are additional **systemFlags** bits that you cannot set, such as the 0x10 bit which indicates whether the attribute or class is category 1 or category 2.</span></span> <span data-ttu-id="c4407-110">Il bit 0x10 è impostato per gli oggetti di categoria 1, ovvero le classi e gli attributi inclusi nello schema di base incluso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c4407-110">The 0x10 bit is set for category 1 objects, which are the classes and attributes included in the base schema included with the system.</span></span> <span data-ttu-id="c4407-111">Il bit non è impostato per le classi e gli attributi della categoria 2, che sono estensioni dello schema.</span><span class="sxs-lookup"><span data-stu-id="c4407-111">The bit is not set for category 2 attributes and classes, which are extensions to the schema.</span></span> <span data-ttu-id="c4407-112">Se non esiste alcuna proprietà **systemFlags** in un oggetto **attributeSchema** o **classSchema** , è la categoria 2.</span><span class="sxs-lookup"><span data-stu-id="c4407-112">If no **systemFlags** property exists on an **attributeSchema** or **classSchema** object, it is category 2.</span></span>

<span data-ttu-id="c4407-113">Il **\_ bit della regola di corrispondenza LDAP \_ \_ \_ e** la regola di corrispondenza possono essere usati per cercare gli oggetti con il flag 0x10 impostato nell'attributo **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="c4407-113">The **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule can be used to search for objects that have the 0x10 flag set in the **systemFlags** attribute.</span></span> <span data-ttu-id="c4407-114">Per altre informazioni, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="c4407-114">For more information, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

## <a name="querying-for-category-1"></a><span data-ttu-id="c4407-115">Esecuzione di query per la categoria 1</span><span class="sxs-lookup"><span data-stu-id="c4407-115">Querying for Category 1</span></span>

<span data-ttu-id="c4407-116">La stringa di query seguente cerca gli attributi di categoria 1 (oggetti **attributeSchema** con il bit 0x10 impostato nella proprietà **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="c4407-116">The following query string searches for category 1 attributes (**attributeSchema** objects with the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



<span data-ttu-id="c4407-117">Tenere presente che, nell'esempio precedente, la sintassi della query LDAP richiede valori decimali. Pertanto, il valore esadecimale del flag deve essere convertito in Decimal.</span><span class="sxs-lookup"><span data-stu-id="c4407-117">Be aware that, in the example above, the LDAP query syntax requires decimal values; therefore, the hex value of the flag must be converted to decimal.</span></span> <span data-ttu-id="c4407-118">In questo caso, la categoria 1 bit è 0x10, quindi il valore del filtro deve essere specificato come 16.</span><span class="sxs-lookup"><span data-stu-id="c4407-118">In this case, category 1 bit is 0x10 so the filter value must be specified as 16.</span></span>

## <a name="querying-for-category-2"></a><span data-ttu-id="c4407-119">Esecuzione di query per la categoria 2</span><span class="sxs-lookup"><span data-stu-id="c4407-119">Querying for Category 2</span></span>

<span data-ttu-id="c4407-120">La stringa di query seguente cerca gli attributi di categoria 2 (oggetti **attributeSchema** per i quali non è impostato il bit 0x10 nella proprietà **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="c4407-120">The following query string searches for category 2 attributes (**attributeSchema** objects that do not have the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



<span data-ttu-id="c4407-121">Tenere presente che questa query restituisce anche oggetti **attributeSchema** che non dispongono di una proprietà **systemFlags** e, pertanto, non hanno il flag specificato impostato.</span><span class="sxs-lookup"><span data-stu-id="c4407-121">Be aware that this query also returns **attributeSchema** objects that do not have a **systemFlags** property, and, therefore, implicitly do not have the specified flag set.</span></span>

 

 