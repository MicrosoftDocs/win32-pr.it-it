---
description: Il registro di sistema contiene dati correlati alle risorse.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Descrizione di una risorsa per il registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315730"
---
# <a name="describing-a-resource-for-the-registry"></a>Descrizione di una risorsa per il registro di sistema

Il registro di sistema contiene dati correlati alle risorse. Questi dati si trovano nella seguente chiave del registro di sistema e vengono conservati in un tipo di dati del registro di sistema speciale denominato **reg \_ Resource \_ List**. Le applicazioni possono ottenere i dati correlati alle risorse tramite il provider del registro di sistema. È possibile aggiungere e modificare le risorse di sistema nel registro di sistema.

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

Nella procedura seguente viene descritto come archiviare le informazioni relative alle risorse nel registro di sistema.

**Per archiviare le informazioni relative alle risorse nel registro di sistema**

1.  Creare una stringa che contiene i campi seguenti.

    

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
    ISA<br />
    EISA<br />
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
    <td>Integer che specifica il numero del bus.</td>
    </tr>
    <tr class="odd">
    <td>Numero descrittore parziale</td>
    <td>Integer che specifica il numero di descrittori.</td>
    </tr>
    <tr class="even">
    <td>Offset o tipo di Unione</td>
    <td>Uno dei valori seguenti:<br/> <dl> Port. Start<br />
    Port. PhysicalAddress<br />
    Port. length<br />
    Interrompi livello<br />
    Interrompi. Vector<br />
    Interrupt. affinità<br />
    Memoria. avvio<br />
    Memory. PhysicalAddress<br />
    Memoria. lunghezza<br />
    Canale DMA<br />
    DMA. Port<br />
    DMA. Reserved1<br />
    DeviceSpecificData. DataSize<br />
    DeviceSpecificData. Reserved1<br />
    DeviceSpecificData. Reserved2<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Inserire la stringa nella chiave appropriata sotto la chiave del registro di sistema.

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

Nell'esempio di codice riportato di seguito viene descritto un descrittore di risorse valido.

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

Nell'esempio di codice seguente viene illustrata la sintassi MOF valida per il recupero di un descrittore di risorse.

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

 

 




