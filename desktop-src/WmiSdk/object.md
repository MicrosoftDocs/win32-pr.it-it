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
# <a name="object"></a>OBJECT

Il tipo di dati OBJECT è un oggetto classe WMI utilizzato per dichiarare le associazioni con tipizzazione debole e gli oggetti incorporati. Non si definisce la classe specifica per un oggetto con tipizzazione debole fino a quando non si crea un'istanza della classe. Gli oggetti incorporati definiti con il tipo di dati OBJECT possono contenere istanze di qualsiasi classe WMI. Per ulteriori informazioni, vedere [oggetti incorporati](embedded-objects.md).

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

 

 



