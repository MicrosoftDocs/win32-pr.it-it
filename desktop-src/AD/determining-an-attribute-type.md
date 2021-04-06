---
title: Determinazione di un tipo di attributo
description: L'attributo systemFlags di un oggetto attributeSchema contiene un set di flag che indicano diverse qualità dell'oggetto attributo, ad esempio se l'attributo è costruito o non replicato.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Determinazione di un tipo di attributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046522"
---
# <a name="determining-an-attribute-type"></a><span data-ttu-id="c5b41-104">Determinazione di un tipo di attributo</span><span class="sxs-lookup"><span data-stu-id="c5b41-104">Determining an Attribute Type</span></span>

<span data-ttu-id="c5b41-105">L'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) di un oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) contiene un set di flag che indicano diverse qualità dell'oggetto attributo, ad esempio se l'attributo è costruito o non replicato.</span><span class="sxs-lookup"><span data-stu-id="c5b41-105">The [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated.</span></span> <span data-ttu-id="c5b41-106">Nella tabella seguente sono elencati i flag dell'attributo **systemFlags** che influiscono sul tipo di archiviazione dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="c5b41-106">The following table lists the flags of the **systemFlags** attribute that affect the storage type of the attribute.</span></span> 

| <span data-ttu-id="c5b41-107">Valore del flag</span><span class="sxs-lookup"><span data-stu-id="c5b41-107">Flag value</span></span> | <span data-ttu-id="c5b41-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5b41-108">Description</span></span>                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b41-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c5b41-109">0x00000001</span></span> | <span data-ttu-id="c5b41-110">Se questo flag è presente nell'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , l'attributo non viene replicato.</span><span class="sxs-lookup"><span data-stu-id="c5b41-110">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is not replicated.</span></span> |
| <span data-ttu-id="c5b41-111">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c5b41-111">0x00000004</span></span> | <span data-ttu-id="c5b41-112">Se questo flag è presente nell'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , l'attributo viene costruito.</span><span class="sxs-lookup"><span data-stu-id="c5b41-112">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is constructed.</span></span>    |



 

<span data-ttu-id="c5b41-113">È possibile creare una stringa di query che può essere usata per eseguire query per attributi costruiti o non replicati.</span><span class="sxs-lookup"><span data-stu-id="c5b41-113">It is possible to construct a query string that can be used to query for constructed or non-replicated attributes.</span></span> <span data-ttu-id="c5b41-114">Ad esempio, la stringa di query seguente trova tutti gli oggetti [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) non replicati.</span><span class="sxs-lookup"><span data-stu-id="c5b41-114">For example, the following query string finds all non-replicated [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects.</span></span> <span data-ttu-id="c5b41-115">Tenere presente che la stringa di query richiede l'equivalente decimale del valore, non l'equivalente esadecimale del valore.</span><span class="sxs-lookup"><span data-stu-id="c5b41-115">Be aware that the query string requires the decimal equivalent of the value, not the hexadecimal equivalent of the value.</span></span> <span data-ttu-id="c5b41-116">Per ulteriori informazioni sull'OID della regola di corrispondenza utilizzato da questa stringa di query, vedere [come specificare i valori di confronto](how-to-specify-comparison-values.md).</span><span class="sxs-lookup"><span data-stu-id="c5b41-116">For more information about the matching rule OID used by this query string, see [How to Specify Comparison Values](how-to-specify-comparison-values.md).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



<span data-ttu-id="c5b41-117">L'attributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) dell'oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di ogni attributo definisce se un attributo è indicizzato; un attributo indicizzato ha un valore pari a 1, un attributo non indicizzato ha un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="c5b41-117">The [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is indexed; an indexed attribute has a value of 1, a non-indexed attribute has a value of 0.</span></span> <span data-ttu-id="c5b41-118">Ad esempio, la stringa di query seguente consente di trovare gli oggetti **attributeSchema** che rappresentano gli attributi indicizzati.</span><span class="sxs-lookup"><span data-stu-id="c5b41-118">For example, the following query string finds the **attributeSchema** objects representing indexed attributes.</span></span>


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



<span data-ttu-id="c5b41-119">L'attributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) dell'oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di ogni attributo definisce se un attributo viene replicato nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="c5b41-119">The [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is replicated to the global catalog.</span></span> <span data-ttu-id="c5b41-120">Questo attributo ha un valore **true** se l'attributo è un membro del catalogo globale o **false** se gli attributi non sono presenti nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="c5b41-120">This attribute has a value of **TRUE** if the attribute is a member of the global catalog or **FALSE** if the attributes is not in the global catalog.</span></span> <span data-ttu-id="c5b41-121">Ad esempio, la stringa di query seguente esegue la ricerca negli oggetti **attributeSchema** replicati nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="c5b41-121">For example, the following query string searches the **attributeSchema** objects that are replicated to the global catalog.</span></span>


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 