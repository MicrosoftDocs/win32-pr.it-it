---
description: Il Registro di sistema contiene dati relativi alle risorse.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Descrizione di una risorsa per il Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30be25eed569f212e435827023eed132cf1c6ead49be37eabb6fe4ac30e8e3b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097271"
---
# <a name="describing-a-resource-for-the-registry"></a>Descrizione di una risorsa per il Registro di sistema

Il Registro di sistema contiene dati relativi alle risorse. Questi dati si trovano nella chiave del Registro di sistema seguente e vengono mantenuti in uno speciale tipo di dati del Registro di sistema denominato **REG \_ RESOURCE \_ LIST**. Le applicazioni possono ottenere i dati relativi alle risorse tramite il provider del Registro di sistema. È possibile aggiungere e modificare le risorse di sistema nel Registro di sistema.

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

La procedura seguente descrive come archiviare le informazioni relative alle risorse nel Registro di sistema.

**Per archiviare le informazioni relative alle risorse nel Registro di sistema**

1.  Creare una stringa contenente i campi seguenti.

    

    <table>
    <thead>
    <tr class="header">
    <th>Campo</th>
    <th>Contiene</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Tipo interfaccia</td>
    <td>Uno dei valori seguenti:<br/> <dl> Interno<br />
    Isa<br />
    Eisa<br />
    MicroChannel<br />
    TurboChannel<br />
    PCIBus<br />
    VMEBus<br />
    NuBus<br />
    PCMCIABus<br />
    CBus<br />
    MPIBus<br />
    MPSABus<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Numero bus</td>
    <td>Numero intero che specifica il numero del bus.</td>
    </tr>
    <tr class="odd">
    <td>Numero di descrittore parziale</td>
    <td>Numero intero che specifica il numero del descrittore.</td>
    </tr>
    <tr class="even">
    <td>Tipo di offset o unione</td>
    <td>Uno dei valori seguenti:<br/> <dl> Port.Start<br />
    Port.PhysicalAddress<br />
    Port.Length<br />
    Interrupt.Level<br />
    Interrupt.Vector<br />
    Interrupt.Affinity<br />
    Memory.Start<br />
    Memory.PhysicalAddress<br />
    Memory.Length<br />
    Dma.Channel<br />
    Dma.Port<br />
    Dma.Reserved1<br />
    DeviceSpecificData.DataSize<br />
    DeviceSpecificData.Reserved1<br />
    DeviceSpecificData.Reserved2<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Inserire la stringa nella chiave appropriata nella chiave del Registro di sistema.

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

Nell'esempio di codice seguente viene descritto un descrittore di risorsa valido.

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

Nell'esempio di codice seguente viene illustrata la sintassi MOF valida per il recupero di un descrittore di risorsa.

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




