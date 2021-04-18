---
description: È possibile filtrare le istanze di una classe di visualizzazione join assegnando una query WQL al qualificatore PostJoinFilter.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Qualificatore PostJoinFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315194"
---
# <a name="postjoinfilter-qualifier"></a><span data-ttu-id="876e8-103">Qualificatore PostJoinFilter</span><span class="sxs-lookup"><span data-stu-id="876e8-103">PostJoinFilter Qualifier</span></span>

<span data-ttu-id="876e8-104">È possibile filtrare le istanze di una classe di visualizzazione join assegnando una query WQL al qualificatore **PostJoinFilter** .</span><span class="sxs-lookup"><span data-stu-id="876e8-104">You can filter the instances of a join view class by assigning a WQL query to the **PostJoinFilter** qualifier.</span></span> <span data-ttu-id="876e8-105">Il valore della query WQL viene applicato alle istanze della classe di visualizzazione join.</span><span class="sxs-lookup"><span data-stu-id="876e8-105">The value of the WQL query is applied to the instances of the join view class.</span></span> <span data-ttu-id="876e8-106">È possibile usare questo qualificatore per limitare le istanze della classe di visualizzazione a quelle che soddisfano determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="876e8-106">You can use this qualifier to restrict the instances of your view class to those that meet specific conditions.</span></span> <span data-ttu-id="876e8-107">La query WQL seguente Filtra le istanze di una classe join chiamata in base alle istanze di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="876e8-107">The following WQL query filters instances of a join class called based on instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



<span data-ttu-id="876e8-108">L'uso di questo qualificatore presenta diverse limitazioni:</span><span class="sxs-lookup"><span data-stu-id="876e8-108">There are several restrictions to the use of this qualifier:</span></span>

-   <span data-ttu-id="876e8-109">**PostJoinFilter** è disponibile solo per le classi di visualizzazione join.</span><span class="sxs-lookup"><span data-stu-id="876e8-109">**PostJoinFilter** is only available to join view classes.</span></span>
-   <span data-ttu-id="876e8-110">Il nome della classe e i nomi di proprietà specificati nella query fanno riferimento alle proprietà della classe di visualizzazione, non alla classe di origine.</span><span class="sxs-lookup"><span data-stu-id="876e8-110">The class name and property names specified in the query refer to the properties of the view class, not the source class.</span></span>
-   <span data-ttu-id="876e8-111">Non sono consentite esclusioni di proprietà; `SELECT *` sono consentite solo query di tipo.</span><span class="sxs-lookup"><span data-stu-id="876e8-111">No exclusion of properties is permitted; only `SELECT *` type queries are allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="876e8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="876e8-112">Requirements</span></span>



| <span data-ttu-id="876e8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="876e8-113">Requirement</span></span> | <span data-ttu-id="876e8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="876e8-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="876e8-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="876e8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="876e8-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="876e8-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="876e8-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="876e8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="876e8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="876e8-118">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="876e8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="876e8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876e8-120">**Qualificatori specifici del provider di visualizzazione**</span><span class="sxs-lookup"><span data-stu-id="876e8-120">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

