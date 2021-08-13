---
description: "Quando si crea un'istanza con oggetti incorporati, eseguire le attività seguenti:"
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Creazione di oggetti incorporati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2e54e16005669ebd77b0bc08e5d3174f7aa5fadee2a47477920e91aaa2ae155b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464171"
---
# <a name="creating-embedded-objects"></a>Creazione di oggetti incorporati

Quando si crea un'istanza con oggetti incorporati, eseguire le attività seguenti:

-   È necessario dichiarare un oggetto incorporato come fortemente tipizzato o tipizzato in modo debole.

    Un oggetto fortemente tipizzato punta a un oggetto di una classe specifica e usa il nome della classe. Un oggetto tipiizzato in modo debole punta a un oggetto di una classe non specificata e usa la parola **chiave object.** Entrambi gli oggetti vengono mappati al **tipo VT \_ UNKNOWN.**

-   È possibile usare **NULL** per il valore predefinito di percorsi e oggetti incorporati nelle inizializzazioni e nelle dichiarazioni.
-   Quando si incorpora un percorso di oggetto, non inserire spazi vuoti tra gli elementi del percorso incorporato. Ad esempio, il percorso dell'oggetto "Class1Index=3;" non contiene spazio tra il nome della proprietà "Class1index" e il valore assegnato, ovvero "3".

La dichiarazione di classe seguente illustra come dichiarare oggetti incorporati fortemente tipizzato e tipizzato in modo debole.

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

Negli esempi seguenti viene descritto come dichiarare oggetti incorporati all'interno di una dichiarazione di classe.

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

Nell'esempio seguente viene descritta l'inizializzazione di una proprietà che è un oggetto fortemente tipizzato e di un'altra proprietà che è una matrice di oggetti tipizzato in modo debole.

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



