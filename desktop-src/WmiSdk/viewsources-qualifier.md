---
description: Tutte le classi di visualizzazione devono avere un qualificatore di matrice di stringhe denominato ViewSources.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Qualificatore ViewSources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757760"
---
# <a name="viewsources-qualifier"></a><span data-ttu-id="4f69c-103">Qualificatore ViewSources</span><span class="sxs-lookup"><span data-stu-id="4f69c-103">ViewSources Qualifier</span></span>

<span data-ttu-id="4f69c-104">Tutte le classi di visualizzazione devono avere un qualificatore di matrice di stringhe denominato **ViewSources**.</span><span class="sxs-lookup"><span data-stu-id="4f69c-104">All view classes must have a string array qualifier called **ViewSources**.</span></span> <span data-ttu-id="4f69c-105">Il qualificatore **ViewSources** contiene le query di origine che definiscono le istanze di origine utilizzate nella classe di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4f69c-105">The **ViewSources** qualifier contains the source queries that define the source instances used in the view class.</span></span> <span data-ttu-id="4f69c-106">Il valore del qualificatore **ViewSources** è una matrice di stringhe contenente le query [*WQL (WMI Query Language)*](gloss-w.md) .</span><span class="sxs-lookup"><span data-stu-id="4f69c-106">The value of the **ViewSources** qualifier is a string array containing [*WMI Query Language (WQL)*](gloss-w.md) queries.</span></span> <span data-ttu-id="4f69c-107">È possibile definire le classi di origine e limitare le istanze di origine utilizzate dalla classe di visualizzazione con la[clausola WHERE](where-clause.md) di [query con WQL](querying-with-wql.md)per creare una visualizzazione filtrata.</span><span class="sxs-lookup"><span data-stu-id="4f69c-107">You can define source classes and restrict the source instances your view class uses with the [Querying with WQL](querying-with-wql.md)[WHERE Clause](where-clause.md) to create a filtered view.</span></span>

<span data-ttu-id="4f69c-108">Il [provider di viste](view-provider.md) corrisponde alle query di origine nel qualificatore **ViewSources** per gli spazi dei nomi elencati nel [qualificatore ViewSpaces](viewspaces-qualifier.md) nell'ordine in cui sono elencate le query e gli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4f69c-108">The [View Provider](view-provider.md) matches the source queries in the **ViewSources** qualifier to the namespaces listed in the [ViewSpaces qualifier](viewspaces-qualifier.md) in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="4f69c-109">Il numero di query di origine deve corrispondere al numero di spazi dei nomi elencati nel qualificatore ViewSpaces.</span><span class="sxs-lookup"><span data-stu-id="4f69c-109">The number of source queries must match the number of namespaces listed in the ViewSpaces qualifier.</span></span> <span data-ttu-id="4f69c-110">L'ordine in cui vengono elencate le query di origine determina gli spazi dei nomi da cui vengono disegnate le istanze di origine.</span><span class="sxs-lookup"><span data-stu-id="4f69c-110">The order in which you list the source queries determines the namespaces from which the source instances are drawn.</span></span>

<span data-ttu-id="4f69c-111">Nell'esempio seguente vengono selezionate solo le istanze della classe **LocalDisk** in cui il valore della proprietà **filesystem** è "NTFS" e le istanze della classe **RemoteDisk** in cui il valore della proprietà **FreeSpace** è maggiore di 45 megabyte:</span><span class="sxs-lookup"><span data-stu-id="4f69c-111">The following example selects only instances of the **LocalDisk** class where the value of the **FileSystem** property is "NTFS" and instances of the **RemoteDisk** class where the value of the **FreeSpace** property is greater than 45 megabytes:</span></span>


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> <span data-ttu-id="4f69c-112">Il numero di query di origine che è possibile definire per le classi di visualizzazione join dipende dal numero di istanze restituite da queste query e dal numero di modi in cui tali istanze possono essere unite in join.</span><span class="sxs-lookup"><span data-stu-id="4f69c-112">The number of source queries you can define for join view classes depends on the number of instances these queries return and how many ways these instances can be joined.</span></span> <span data-ttu-id="4f69c-113">Il numero di possibili combinazioni di istanze di origine per le classi di visualizzazione cresce in modo esponenziale, quindi è possibile usare le query di origine per le classi di visualizzazione join il più semplice possibile.</span><span class="sxs-lookup"><span data-stu-id="4f69c-113">The number of possible combinations of source instances for view classes grows exponentially, so keep source queries for join view classes as simple as possible.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f69c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f69c-114">Requirements</span></span>



| <span data-ttu-id="4f69c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f69c-115">Requirement</span></span> | <span data-ttu-id="4f69c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4f69c-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4f69c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f69c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4f69c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f69c-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4f69c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f69c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4f69c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f69c-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f69c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f69c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f69c-122">**Qualificatori specifici del provider di visualizzazione**</span><span class="sxs-lookup"><span data-stu-id="4f69c-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




