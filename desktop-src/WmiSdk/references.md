---
description: La parola chiave di riferimento MOF descrive il percorso di un oggetto ed esegue il mapping a un tipo di \_ automazione BSTR VT.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Riferimenti (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea004a4d0a1cf160d387b07e9c9d7ac85eaaaf21851bd315ecd1bb4ba6f2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050459"
---
# <a name="references-wmi"></a>Riferimenti (WMI)

La parola chiave di **riferimento** MOF descrive il percorso di un oggetto ed esegue il mapping a un tipo di \_ automazione BSTR VT. Il percorso dell'oggetto può essere un percorso completo di un server e uno spazio dei nomi o un percorso relativo a un altro oggetto nello stesso spazio dei nomi. È possibile usare una **parola chiave di** riferimento per collegare due o più classi. WMI supporta due tipi di percorsi oggetto, che consentono di definire percorsi generali o specifici all'interno di WMI.

Lo scopo principale della parola **chiave ref** è ridurre il tempo di trasporto e la codifica tra gli oggetti esistenti interamente nel repository WMI. È anche possibile usare la **parola chiave ref** per creare un'associazione tra due classi. Per altre informazioni, vedere [Dichiarazione di una classe di associazione](declaring-an-association-class.md). Se l'elemento a cui si fa riferimento si trova all'interno dello stesso file MOF, usare un alias per inizializzare il **valore di** riferimento. Per altre informazioni, vedere [Creazione di un alias](creating-an-alias.md).

> [!Note]  
> Quando una **parola chiave** di riferimento viene applicata a una proprietà chiave, è possibile distinguere i riferimenti agli oggetti in base al valore della stringa dell'oggetto anziché al valore dereferenziato.

 

MOF supporta il concetto di percorso di oggetto tipizzato in modo debole e fortemente tipizzato. Un percorso di oggetto tipiizzato in modo debole punta a un oggetto di una classe non specificata e usa la parola chiave **ref** con la [parola chiave OBJECT.](object.md) Un oggetto fortemente tipizzato punta a un oggetto di una classe specifica e usa **ref** con il nome della classe. L'esempio seguente descrive un riferimento **RefToAnyClass** tipizzata in modo debole che può puntare a qualsiasi classe o istanza di classe e un riferimento **RefToClassX** che può puntare solo a una classe o a un'istanza **ClassX:**

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

Nell'esempio seguente vengono descritte due istanze e un oggetto associazione che fa riferimento alle istanze precedenti:

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



