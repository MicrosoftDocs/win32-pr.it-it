---
description: "Quando si crea un'istanza di con oggetti incorporati, eseguire le attività seguenti:"
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
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316568"
---
# <a name="creating-embedded-objects"></a>Creazione di oggetti incorporati

Quando si crea un'istanza di con oggetti incorporati, eseguire le attività seguenti:

-   È necessario dichiarare un oggetto incorporato come fortemente tipizzato o debolmente tipizzato.

    Un oggetto fortemente tipizzato punta a un oggetto di una classe specifica e usa il nome della classe. Un oggetto con tipizzazione debole punta a un oggetto di una classe non specificata e utilizza la parola chiave **Object** . Entrambi gli oggetti sono mappati al tipo **\_ sconosciuto VT** .

-   È possibile utilizzare **null** come valore predefinito di oggetti e percorsi incorporati nelle inizializzazioni e nelle dichiarazioni.
-   Quando si incorpora un percorso di oggetto, non inserire spazi vuoti tra gli elementi del percorso incorporato. Il percorso dell'oggetto "Class1Index = 3;", ad esempio, non contiene alcuno spazio tra il nome della proprietà "Class1index" e il valore assegnato, ovvero "3".

Nella dichiarazione di classe seguente viene illustrato come dichiarare oggetti incorporati fortemente tipizzati e con tipizzazione debole.

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

Nell'esempio seguente viene descritta l'inizializzazione di una proprietà che è un oggetto fortemente tipizzato e un'altra proprietà che è una matrice di oggetti con tipizzazione debole.

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

 

 



