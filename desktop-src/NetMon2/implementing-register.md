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
# <a name="implementing-register"></a>Implementazione del registro

Network Monitor carica un'acquisizione dal file di acquisizione, quindi avvia la chiamata della funzione [**Register**](register-parser.md) per tutti i protocolli che è in grado di identificare. Ogni DLL del parser deve implementare una funzione **Register** per ogni protocollo supportato dalla dll del parser.

Ogni implementazione della funzione [**Register**](register-parser.md) deve chiamare le funzioni [**CreatePropertyDatabase**](createpropertydatabase.md) e [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) per creare e compilare il [*database delle proprietà*](p.md) per il protocollo, quindi [**CreateHandoffTable**](createhandofftable.md) per creare la [*tabella*](h.md) di consegna per il protocollo, se necessario.

> [!Note]  
> Le proprietà del protocollo sono definite per Network Monitor. Non viene eseguito il mapping delle proprietà a un percorso in un dato di acquisizione fino a quando non viene chiamata la funzione di esportazione [**AttachProperties**](attachproperties.md) .

 

Nella procedura seguente vengono identificati i passaggi necessari per implementare la funzione [**Register**](register-parser.md) .

**Per implementare la registrazione per un protocollo**

1.  Definire una matrice di strutture [**PROPERTYINFO**](propertyinfo.md) per descrivere ogni proprietà supportata dal protocollo.
2.  Chiamare [**CreatePropertyDatabase**](createpropertydatabase.md) per fornire un handle di protocollo e il numero di proprietà supportate dal protocollo.
3.  Chiamare [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in un ciclo per aggiungere ogni proprietà definita nella matrice della struttura [**PROPERTYINFO**](propertyinfo.md) .
4.  Se il protocollo utilizza una tabella con continuità, chiamare [**CreateHandoffTable**](createhandofftable.md), dopo che tutte le proprietà del protocollo vengono aggiunte al database della proprietà.

Di seguito è riportata un'implementazione di base di [**Register**](register-parser.md). Si noti che viene creato un database di proprietà per un protocollo che supporta solo due proprietà. Questo esempio di codice viene tratto dal parser generico fornito da Network Monitor.

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

 

 
