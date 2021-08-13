---
description: Il tipo di dati OBJECT è un oggetto classe WMI utilizzato per dichiarare associazioni con tipi di dati deboli e oggetti incorporati.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c26b8b6ff77f788aeed607057541d19d80fea4c105b53d492c1f1e8468b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554930"
---
# <a name="object"></a>OBJECT

Il tipo di dati OBJECT è un oggetto classe WMI utilizzato per dichiarare associazioni con tipi di dati deboli e oggetti incorporati. Non si definisce la classe specifica per un oggetto con tipi di dati debole fino a quando non si crea un'istanza della classe. Gli oggetti incorporati definiti con il tipo di dati OBJECT possono contenere istanze di qualsiasi classe WMI. Per altre informazioni, vedere [Oggetti incorporati.](embedded-objects.md)

Nell'esempio seguente vengono definite e create istanze di due classi, una delle quali contiene un oggetto incorporato di tipo OBJECT:

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

 

 



