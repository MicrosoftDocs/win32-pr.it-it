---
description: Il modello di localizzazione dello schema CIM fornisce un meccanismo per localizzare i qualificatori. Non supporta la localizzazione diretta dei valori delle proprietà.
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: Localizzazione dei valori delle proprietà
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344896"
---
# <a name="localizing-property-values"></a><span data-ttu-id="d3d23-104">Localizzazione dei valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d3d23-104">Localizing Property Values</span></span>

<span data-ttu-id="d3d23-105">Il modello di localizzazione dello schema CIM fornisce un meccanismo per localizzare i qualificatori.</span><span class="sxs-lookup"><span data-stu-id="d3d23-105">The CIM schema localization model provides a mechanism for localizing qualifiers.</span></span> <span data-ttu-id="d3d23-106">Non supporta la localizzazione diretta dei valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3d23-106">It does not support direct localization of property values.</span></span>

<span data-ttu-id="d3d23-107">In alcuni casi, tuttavia, i valori delle proprietà di stringa nelle istanze statiche possono essere sostituiti da un tipo Integer enumerato ed è possibile definire una mappa di valori per la proprietà nella definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="d3d23-107">In some cases, however, the string properties values in the static instances can be replaced by an enumerated integer type and a value map can be defined for the property in the class definition.</span></span> <span data-ttu-id="d3d23-108">In questi casi, il qualificatore **values** deve essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="d3d23-108">In these cases, the **Values** qualifier should be localized.</span></span> <span data-ttu-id="d3d23-109">L'uso di qualificatori di enumerazione è il meccanismo principale per localizzare i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3d23-109">Using enumeration qualifiers is the primary mechanism for localizing property values.</span></span> <span data-ttu-id="d3d23-110">Qualsiasi altra forma di localizzazione del valore della proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="d3d23-110">Any other forms of property value localization are not supported.</span></span>

<span data-ttu-id="d3d23-111">Nell'esempio seguente viene illustrato il modo in cui le proprietà statiche possono essere localizzate utilizzando le mappe di valori parziali con espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="d3d23-111">The following example shows how static properties can be localized using partial value maps with regular expressions.</span></span> <span data-ttu-id="d3d23-112">In questo esempio, il subset di valori predefinito viene inizializzato nello schema usando istanze statiche.</span><span class="sxs-lookup"><span data-stu-id="d3d23-112">In this example, the predefined subset of values is initialized in the schema using static instances.</span></span> <span data-ttu-id="d3d23-113">Il resto dei valori viene fornito dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d3d23-113">The rest of the values are provided dynamically.</span></span>

``` syntax
[abstract]
class DataGroup
{
   [key] string GUID;
   [Description("data group display name"): Amended,
                     ValueMap{"Logical Disk",
                     "CPU Utilization", ".+"}]
                     string GroupDisplayName;
   [ValueMap{"Monitors percentage of disk free space",
                  "Monitors percentage CPU utilization", ".+"}] 
                   string GroupDescription;
};

[static, Description ("pre-configured parameters") :amended]
class InitialGroup : DataGroup {
};

[dynamic, provider("HMProvider"),
    Description ("user-defined parameters") :amended]
class UserDefionedGroup : DataGroup {
};

instance of InitialGroup {
   GUID = "abc";
   GroupDisplayName = "Logical Disk";
   GroupDescription = "Monitors percentage of disk free space";
};

instance of InitialGroup {
   GUID = "def";
   GroupDisplayName = "CPU Utilization";
   GroupDescription = "Monitors percentage CPU utilization";
};
```

<span data-ttu-id="d3d23-114">Per altre informazioni, vedere [localizzazione di proprietà statiche](localizing-static-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d3d23-114">For more information, see [Localizing Static Properties](localizing-static-properties.md).</span></span>

 

 



