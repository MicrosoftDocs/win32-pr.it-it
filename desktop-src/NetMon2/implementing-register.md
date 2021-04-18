---
description: Network Monitor carica un'acquisizione dal file di acquisizione, quindi avvia la chiamata della funzione Register per tutti i protocolli che è in grado di identificare. Ogni DLL del parser deve implementare una funzione Register per ogni protocollo supportato dalla DLL del parser.
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: Implementazione del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59f34f5f97925627184db7188aac0a9eb796a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318255"
---
# <a name="implementing-register"></a><span data-ttu-id="40952-104">Implementazione del registro</span><span class="sxs-lookup"><span data-stu-id="40952-104">Implementing Register</span></span>

<span data-ttu-id="40952-105">Network Monitor carica un'acquisizione dal file di acquisizione, quindi avvia la chiamata della funzione [**Register**](register-parser.md) per tutti i protocolli che è in grado di identificare.</span><span class="sxs-lookup"><span data-stu-id="40952-105">Network Monitor loads a capture from the capture file, and then starts calling the [**Register**](register-parser.md) function for all the protocols that it can identify.</span></span> <span data-ttu-id="40952-106">Ogni DLL del parser deve implementare una funzione **Register** per ogni protocollo supportato dalla dll del parser.</span><span class="sxs-lookup"><span data-stu-id="40952-106">Each parser DLL must implement a **Register** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="40952-107">Ogni implementazione della funzione [**Register**](register-parser.md) deve chiamare le funzioni [**CreatePropertyDatabase**](createpropertydatabase.md) e [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) per creare e compilare il [*database delle proprietà*](p.md) per il protocollo, quindi [**CreateHandoffTable**](createhandofftable.md) per creare la [*tabella*](h.md) di consegna per il protocollo, se necessario.</span><span class="sxs-lookup"><span data-stu-id="40952-107">Each implementation of the [**Register**](register-parser.md) function must call the [**CreatePropertyDatabase**](createpropertydatabase.md) and [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) functions to create and fill-in the [*property database*](p.md) for the protocol, and then the [**CreateHandoffTable**](createhandofftable.md) to create the [*handoff table*](h.md) for the protocol — if needed.</span></span>

> [!Note]  
> <span data-ttu-id="40952-108">Le proprietà del protocollo sono definite per Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="40952-108">Protocol properties are defined for Network Monitor.</span></span> <span data-ttu-id="40952-109">Non viene eseguito il mapping delle proprietà a un percorso in un dato di acquisizione fino a quando non viene chiamata la funzione di esportazione [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="40952-109">Properties are not mapped to a location in a capture data until the [**AttachProperties**](attachproperties.md) export function is called.</span></span>

 

<span data-ttu-id="40952-110">Nella procedura seguente vengono identificati i passaggi necessari per implementare la funzione [**Register**](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="40952-110">The following procedure identifies the steps necessary to implement the [**Register**](register-parser.md) function.</span></span>

<span data-ttu-id="40952-111">**Per implementare la registrazione per un protocollo**</span><span class="sxs-lookup"><span data-stu-id="40952-111">**To implement Register for one protocol**</span></span>

1.  <span data-ttu-id="40952-112">Definire una matrice di strutture [**PROPERTYINFO**](propertyinfo.md) per descrivere ogni proprietà supportata dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="40952-112">Define an array of [**PROPERTYINFO**](propertyinfo.md) structures to describe each property that the protocol supports.</span></span>
2.  <span data-ttu-id="40952-113">Chiamare [**CreatePropertyDatabase**](createpropertydatabase.md) per fornire un handle di protocollo e il numero di proprietà supportate dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="40952-113">Call [**CreatePropertyDatabase**](createpropertydatabase.md) to provide a protocol handle, and the number of properties that the protocol supports.</span></span>
3.  <span data-ttu-id="40952-114">Chiamare [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in un ciclo per aggiungere ogni proprietà definita nella matrice della struttura [**PROPERTYINFO**](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="40952-114">Call [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in a loop to add each property defined in the [**PROPERTYINFO**](propertyinfo.md) structure array.</span></span>
4.  <span data-ttu-id="40952-115">Se il protocollo utilizza una tabella con continuità, chiamare [**CreateHandoffTable**](createhandofftable.md), dopo che tutte le proprietà del protocollo vengono aggiunte al database della proprietà.</span><span class="sxs-lookup"><span data-stu-id="40952-115">If the protocol uses a handoff table, call [**CreateHandoffTable**](createhandofftable.md)— after all the properties of the protocol are added to the property database.</span></span>

<span data-ttu-id="40952-116">Di seguito è riportata un'implementazione di base di [**Register**](register-parser.md).</span><span class="sxs-lookup"><span data-stu-id="40952-116">The following is a basic implementation of [**Register**](register-parser.md).</span></span> <span data-ttu-id="40952-117">Si noti che viene creato un database di proprietà per un protocollo che supporta solo due proprietà.</span><span class="sxs-lookup"><span data-stu-id="40952-117">Note that a property database is created for a protocol that supports only two properties.</span></span> <span data-ttu-id="40952-118">Questo esempio di codice viene tratto dal parser generico fornito da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="40952-118">This code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PROPERTYINFO MyProtocolPropertyTable[]
{
  // Summary property (0)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "Summary",                       // Property label.
     "Summary of protocol packet",    // Property comment.
     PROP_TYPE_SUMMARY,               // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

  // WORD property (1)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "WORD property",                 // Property label.
     "16-bit WORD property",         // Property comment.
     PROP_TYPE_WORD,                  // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

}

void BHAPI MyProtocolRegister( HPPROTOCOL hProtocol) 
{
  // Create property database.
  DWORD dwNumberOfProperties = 2;
  CreatePropertyDatabase (hProtocol,
                          dwNumberOfProperties
                          );
  
  // Add properties to database.
  WORD i;
  for( i=0; i< dwNumberOfProperties; i++)
  {
     AddProperty(hProtocol, &MyProtocolPropertyTable[i]);
  }

  // Create handoff table.
  CreateHandoffTable("myProtocolHandoffTable",
                          "myProtocol.ini",
                           hTable,
                           MaxEntries,
                           10       // Handoff set values are base 10.
                          )
}
```

 

 
