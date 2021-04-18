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
# <a name="describing-a-resource-for-the-registry"></a><span data-ttu-id="48f4b-103">Descrizione di una risorsa per il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="48f4b-103">Describing a Resource for the Registry</span></span>

<span data-ttu-id="48f4b-104">Il registro di sistema contiene dati correlati alle risorse.</span><span class="sxs-lookup"><span data-stu-id="48f4b-104">The system registry contains resource-related data.</span></span> <span data-ttu-id="48f4b-105">Questi dati si trovano nella seguente chiave del registro di sistema e vengono conservati in un tipo di dati del registro di sistema speciale denominato **reg \_ Resource \_ List**.</span><span class="sxs-lookup"><span data-stu-id="48f4b-105">This data is located under the following registry key and is kept in a special registry data type named **REG\_RESOURCE\_LIST**.</span></span> <span data-ttu-id="48f4b-106">Le applicazioni possono ottenere i dati correlati alle risorse tramite il provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="48f4b-106">Applications can obtain the resource-related data through the System Registry provider.</span></span> <span data-ttu-id="48f4b-107">È possibile aggiungere e modificare le risorse di sistema nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="48f4b-107">You can add and modify system resources in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

<span data-ttu-id="48f4b-108">Nella procedura seguente viene descritto come archiviare le informazioni relative alle risorse nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="48f4b-108">The following procedure describes how to store resource-related information in the system registry.</span></span>

<span data-ttu-id="48f4b-109">**Per archiviare le informazioni relative alle risorse nel registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="48f4b-109">**To store resource-related information in the system registry**</span></span>

1.  <span data-ttu-id="48f4b-110">Creare una stringa che contiene i campi seguenti.</span><span class="sxs-lookup"><span data-stu-id="48f4b-110">Create a string that contains the following fields.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="48f4b-111">Campo</span><span class="sxs-lookup"><span data-stu-id="48f4b-111">Field</span></span></th>
    <th><span data-ttu-id="48f4b-112">Contiene</span><span class="sxs-lookup"><span data-stu-id="48f4b-112">Contains</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="48f4b-113">Tipo interfaccia</span><span class="sxs-lookup"><span data-stu-id="48f4b-113">Interface type</span></span></td>
    <td><span data-ttu-id="48f4b-114">Uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="48f4b-114">One of the following values:</span></span><br/> <dl> <span data-ttu-id="48f4b-115">Interno</span><span class="sxs-lookup"><span data-stu-id="48f4b-115">Internal</span></span><br />
    <span data-ttu-id="48f4b-116">ISA</span><span class="sxs-lookup"><span data-stu-id="48f4b-116">Isa</span></span><br />
    <span data-ttu-id="48f4b-117">EISA</span><span class="sxs-lookup"><span data-stu-id="48f4b-117">Eisa</span></span><br />
    <span data-ttu-id="48f4b-118">MicroChannel</span><span class="sxs-lookup"><span data-stu-id="48f4b-118">MicroChannel</span></span><br />
    <span data-ttu-id="48f4b-119">TurboChannel</span><span class="sxs-lookup"><span data-stu-id="48f4b-119">TurboChannel</span></span><br />
    <span data-ttu-id="48f4b-120">PCIBus</span><span class="sxs-lookup"><span data-stu-id="48f4b-120">PCIBus</span></span><br />
    <span data-ttu-id="48f4b-121">VMEBus</span><span class="sxs-lookup"><span data-stu-id="48f4b-121">VMEBus</span></span><br />
    <span data-ttu-id="48f4b-122">NuBus</span><span class="sxs-lookup"><span data-stu-id="48f4b-122">NuBus</span></span><br />
    <span data-ttu-id="48f4b-123">PCMCIABus</span><span class="sxs-lookup"><span data-stu-id="48f4b-123">PCMCIABus</span></span><br />
    <span data-ttu-id="48f4b-124">CBus</span><span class="sxs-lookup"><span data-stu-id="48f4b-124">CBus</span></span><br />
    <span data-ttu-id="48f4b-125">MPIBus</span><span class="sxs-lookup"><span data-stu-id="48f4b-125">MPIBus</span></span><br />
    <span data-ttu-id="48f4b-126">MPSABus</span><span class="sxs-lookup"><span data-stu-id="48f4b-126">MPSABus</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="48f4b-127">Numero bus</span><span class="sxs-lookup"><span data-stu-id="48f4b-127">Bus number</span></span></td>
    <td><span data-ttu-id="48f4b-128">Integer che specifica il numero del bus.</span><span class="sxs-lookup"><span data-stu-id="48f4b-128">Integer specifying the bus number.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="48f4b-129">Numero descrittore parziale</span><span class="sxs-lookup"><span data-stu-id="48f4b-129">Partial descriptor number</span></span></td>
    <td><span data-ttu-id="48f4b-130">Integer che specifica il numero di descrittori.</span><span class="sxs-lookup"><span data-stu-id="48f4b-130">Integer specifying the descriptor number.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="48f4b-131">Offset o tipo di Unione</span><span class="sxs-lookup"><span data-stu-id="48f4b-131">Offset or union type</span></span></td>
    <td><span data-ttu-id="48f4b-132">Uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="48f4b-132">One of the following values:</span></span><br/> <dl> <span data-ttu-id="48f4b-133">Port. Start</span><span class="sxs-lookup"><span data-stu-id="48f4b-133">Port.Start</span></span><br />
    <span data-ttu-id="48f4b-134">Port. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="48f4b-134">Port.PhysicalAddress</span></span><br />
    <span data-ttu-id="48f4b-135">Port. length</span><span class="sxs-lookup"><span data-stu-id="48f4b-135">Port.Length</span></span><br />
    <span data-ttu-id="48f4b-136">Interrompi livello</span><span class="sxs-lookup"><span data-stu-id="48f4b-136">Interrupt.Level</span></span><br />
    <span data-ttu-id="48f4b-137">Interrompi. Vector</span><span class="sxs-lookup"><span data-stu-id="48f4b-137">Interrupt.Vector</span></span><br />
    <span data-ttu-id="48f4b-138">Interrupt. affinità</span><span class="sxs-lookup"><span data-stu-id="48f4b-138">Interrupt.Affinity</span></span><br />
    <span data-ttu-id="48f4b-139">Memoria. avvio</span><span class="sxs-lookup"><span data-stu-id="48f4b-139">Memory.Start</span></span><br />
    <span data-ttu-id="48f4b-140">Memory. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="48f4b-140">Memory.PhysicalAddress</span></span><br />
    <span data-ttu-id="48f4b-141">Memoria. lunghezza</span><span class="sxs-lookup"><span data-stu-id="48f4b-141">Memory.Length</span></span><br />
    <span data-ttu-id="48f4b-142">Canale DMA</span><span class="sxs-lookup"><span data-stu-id="48f4b-142">Dma.Channel</span></span><br />
    <span data-ttu-id="48f4b-143">DMA. Port</span><span class="sxs-lookup"><span data-stu-id="48f4b-143">Dma.Port</span></span><br />
    <span data-ttu-id="48f4b-144">DMA. Reserved1</span><span class="sxs-lookup"><span data-stu-id="48f4b-144">Dma.Reserved1</span></span><br />
    <span data-ttu-id="48f4b-145">DeviceSpecificData. DataSize</span><span class="sxs-lookup"><span data-stu-id="48f4b-145">DeviceSpecificData.DataSize</span></span><br />
    <span data-ttu-id="48f4b-146">DeviceSpecificData. Reserved1</span><span class="sxs-lookup"><span data-stu-id="48f4b-146">DeviceSpecificData.Reserved1</span></span><br />
    <span data-ttu-id="48f4b-147">DeviceSpecificData. Reserved2</span><span class="sxs-lookup"><span data-stu-id="48f4b-147">DeviceSpecificData.Reserved2</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="48f4b-148">Inserire la stringa nella chiave appropriata sotto la chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="48f4b-148">Place the string in the appropriate key under the registry key.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

<span data-ttu-id="48f4b-149">Nell'esempio di codice riportato di seguito viene descritto un descrittore di risorse valido.</span><span class="sxs-lookup"><span data-stu-id="48f4b-149">The following code example describes a valid resource descriptor.</span></span>

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

<span data-ttu-id="48f4b-150">Nell'esempio di codice seguente viene illustrata la sintassi MOF valida per il recupero di un descrittore di risorse.</span><span class="sxs-lookup"><span data-stu-id="48f4b-150">The following code example shows valid MOF syntax for retrieving a resource descriptor.</span></span>

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

 

 




