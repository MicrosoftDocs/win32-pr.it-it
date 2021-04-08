---
description: Il tipo di dati OBJECT è un oggetto classe WMI utilizzato per dichiarare le associazioni con tipizzazione debole e gli oggetti incorporati.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749514"
---
# <a name="object"></a><span data-ttu-id="e5068-103">OBJECT</span><span class="sxs-lookup"><span data-stu-id="e5068-103">OBJECT</span></span>

<span data-ttu-id="e5068-104">Il tipo di dati OBJECT è un oggetto classe WMI utilizzato per dichiarare le associazioni con tipizzazione debole e gli oggetti incorporati.</span><span class="sxs-lookup"><span data-stu-id="e5068-104">The OBJECT data type is a WMI class object use to declare weakly typed associations and embedded objects.</span></span> <span data-ttu-id="e5068-105">Non si definisce la classe specifica per un oggetto con tipizzazione debole fino a quando non si crea un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="e5068-105">You do not define the specific class for a weakly typed object until you create an instance of the class.</span></span> <span data-ttu-id="e5068-106">Gli oggetti incorporati definiti con il tipo di dati OBJECT possono contenere istanze di qualsiasi classe WMI.</span><span class="sxs-lookup"><span data-stu-id="e5068-106">Embedded objects defined with the OBJECT data type can contain instances of any WMI class.</span></span> <span data-ttu-id="e5068-107">Per ulteriori informazioni, vedere [oggetti incorporati](embedded-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e5068-107">For more information, see [Embedded Objects](embedded-objects.md).</span></span>

<span data-ttu-id="e5068-108">Nell'esempio seguente vengono definite e create istanze di due classi, una delle quali contiene un oggetto incorporato di tipo OBJECT:</span><span class="sxs-lookup"><span data-stu-id="e5068-108">The following example defines and creates instances of two classes, one of which contains an embedded object of type OBJECT:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

class CompositeClass
{
    [key] string aKey;   
    object EmbObj;       // Weakly typed
};

class EmbClass

{
  [key] string aKey;
};

instance of CompositeClass
{
    aKey = "CompositeClass Key";
    EmbObj = 
        instance of EmbClass
        {
           aKey = "key for embedded object";
        };
};
```

 

 



