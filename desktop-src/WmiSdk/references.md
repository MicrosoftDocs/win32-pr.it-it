---
description: La parola chiave ref MOF descrive il percorso di un oggetto ed esegue il mapping a un \_ tipo di automazione VT BSTR.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Riferimenti (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883230"
---
# <a name="references-wmi"></a>Riferimenti (WMI)

La parola chiave **ref** MOF descrive il percorso di un oggetto ed esegue il mapping a un \_ tipo di automazione VT BSTR. Il percorso dell'oggetto può essere un percorso completo di un server e uno spazio dei nomi oppure un percorso relativo di un altro oggetto nello stesso spazio dei nomi. È possibile utilizzare una parola chiave **ref** per collegare due o più classi. WMI supporta due tipi di percorsi degli oggetti, che consentono di definire percorsi generali o specifici all'interno di WMI.

Lo scopo principale della parola chiave **ref** è quello di ridurre il tempo di trasporto e la codifica tra gli oggetti presenti interamente nel repository WMI. È anche possibile usare la parola chiave **ref** per creare un'associazione tra due classi. Per ulteriori informazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md). Se l'elemento a cui si fa riferimento si trova all'interno dello stesso file MOF, utilizzare un alias per inizializzare il valore **ref** . Per ulteriori informazioni, vedere [creazione di un alias](creating-an-alias.md).

> [!Note]  
> Quando una parola chiave **ref** viene applicata a una proprietà chiave, è possibile distinguere i riferimenti agli oggetti in base al valore della stringa dell'oggetto anziché al valore dereferenziato.

 

MOF supporta il concetto di percorso di un oggetto tipizzato in modo debole e fortemente tipizzato. Un percorso di oggetto con tipizzazione debole punta a un oggetto di una classe non specificata e usa la parola chiave **ref** con la parola chiave [Object](object.md) . Un oggetto fortemente tipizzato punta a un oggetto di una classe specifica e USA **ref** con il nome della classe. Nell'esempio seguente viene descritto un riferimento **RefToAnyClass** debolmente tipizzato che può puntare a qualsiasi istanza di classe o classe e un riferimento **RefToClassX** che può puntare solo a una classe o istanza di **classx** :

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

Nell'esempio seguente vengono descritte due istanze e un oggetto Association che fanno riferimento alle istanze precedenti:

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

 

 



