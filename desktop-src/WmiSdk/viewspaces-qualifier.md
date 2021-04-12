---
description: Il qualificatore ViewSpaces definisce i nomi e il percorso degli spazi dei nomi in cui si trovano le istanze di origine. È possibile specificare qualsiasi combinazione di spazi dei nomi in computer locali o remoti.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Qualificatore ViewSpaces
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233794"
---
# <a name="viewspaces-qualifier"></a><span data-ttu-id="8ca97-104">Qualificatore ViewSpaces</span><span class="sxs-lookup"><span data-stu-id="8ca97-104">ViewSpaces Qualifier</span></span>

<span data-ttu-id="8ca97-105">Il **qualificatore ViewSpaces** definisce i nomi e il percorso degli spazi dei nomi in cui si trovano le istanze di origine.</span><span class="sxs-lookup"><span data-stu-id="8ca97-105">The **ViewSpaces qualifier** defines the names and location of the namespaces where the source instances are located.</span></span> <span data-ttu-id="8ca97-106">È possibile specificare qualsiasi combinazione di spazi dei nomi in computer locali o remoti.</span><span class="sxs-lookup"><span data-stu-id="8ca97-106">You can specify any combination of namespaces on local or remote computers.</span></span>

<span data-ttu-id="8ca97-107">Nell'esempio seguente vengono elencati due spazi dei nomi nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8ca97-107">The following example lists two namespaces on the local computer.</span></span>


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



<span data-ttu-id="8ca97-108">Il [provider di viste](view-provider.md) corrisponde alle query di origine nel [qualificatore ViewSources](viewsources-qualifier.md) per gli spazi dei nomi elencati nel qualificatore **ViewSpaces** nell'ordine in cui sono elencate le query e gli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8ca97-108">The [View provider](view-provider.md) matches the source queries in the [ViewSources qualifier](viewsources-qualifier.md) to the namespaces listed in the **ViewSpaces** qualifier in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="8ca97-109">In genere, esiste una relazione uno-a-uno tra il numero di spazi dei nomi elencati nel qualificatore **ViewSpaces** e le query elencate nel qualificatore **ViewSources** .</span><span class="sxs-lookup"><span data-stu-id="8ca97-109">Normally, there is a one-to-one relationship between the number of namespaces listed in the **ViewSpaces** qualifier and the queries listed in the **ViewSources** qualifier.</span></span> <span data-ttu-id="8ca97-110">In alcuni casi, potrebbe essere necessario che le query elencate nel qualificatore ViewSources vengano eseguite su due o più spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8ca97-110">In some cases, you may want the queries listed in the ViewSources qualifier to execute against two or more namespaces.</span></span> <span data-ttu-id="8ca97-111">È possibile usare un doppio segno di due punti "::" per separare più spazi dei nomi che verranno valutati da una delle query nella matrice **ViewSources** .</span><span class="sxs-lookup"><span data-stu-id="8ca97-111">You can use a double colon "::" to separate multiple namespaces that will be evaluated by one of the queries in the **ViewSources** array.</span></span>

<span data-ttu-id="8ca97-112">Nell'esempio seguente, la prima query nella matrice [**ViewSources**](viewsources-qualifier.md) verrà eseguita sullo spazio dei nomi nella prima coppia di virgolette, la seconda query sui tre spazi dei nomi nella seconda coppia di virgolette e la terza query sui due spazi dei nomi nella terza coppia di virgolette.</span><span class="sxs-lookup"><span data-stu-id="8ca97-112">In the following example, the first query in the [**ViewSources**](viewsources-qualifier.md) array will be run against the namespace in the first pair of quotes, the second query against the three namespaces in the second pair of quotes, and the third query against the two namespaces in the third pair of quotes.</span></span>


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a><span data-ttu-id="8ca97-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ca97-113">Requirements</span></span>



| <span data-ttu-id="8ca97-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca97-114">Requirement</span></span> | <span data-ttu-id="8ca97-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8ca97-115">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8ca97-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ca97-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca97-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ca97-117">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8ca97-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ca97-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca97-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ca97-119">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ca97-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ca97-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca97-121">**Qualificatori specifici del provider di visualizzazione**</span><span class="sxs-lookup"><span data-stu-id="8ca97-121">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




