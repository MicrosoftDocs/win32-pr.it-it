---
description: Network Monitor chiama la funzione FormatProperties per formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia Network Monitor interfaccia utente.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementazione di FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50e7b927f15ccb2c216e345b37bc87593e33339671f906e28d33759ca9db0abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778976"
---
# <a name="implementing-formatproperties"></a>Implementazione di FormatProperties

Network Monitor chiama la [**funzione FormatProperties**](formatproperties.md) per formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia Network Monitor interfaccia utente. In genere, **FormatProperties** viene chiamato per formattare la riga di riepilogo per un protocollo e quindi per formattare tutte le istanze di proprietà del protocollo all'interno di un frame. Tuttavia, Network Monitor non identifica il numero di volte in cui **FormatProperties** viene chiamato per un parser specifico.

Quando si [**chiama FormatProperties,**](formatproperties.md)Network Monitor una [**struttura PROPERTYINST**](propertyinst.md) per ogni proprietà visualizzata. La **struttura PROPERTYINST** fornisce informazioni sui dati da visualizzare, incluso un puntatore alla struttura [**PROPERTYINFO**](propertyinfo.md) che specifica la funzione da utilizzare per formattare la proprietà dei dati visualizzata.

> [!Note]  
> Una [**struttura PROPERTYINFO**](propertyinfo.md) viene specificata quando si aggiunge una proprietà al [*database delle proprietà*](p.md) del parser.

 

Network Monitor identifica la funzione di formato da chiamare per ogni istanza della proprietà. Il **membro InstanceData** della [**struttura PROPERTYINFO**](propertyinfo.md) può specificare quanto segue:

-   Funzione [**FormatPropertyInstance**](formatpropertyinstance.md) per usare il [*formattatore generico*](g.md) Network Monitor fornisce.

    - oppure -

-   Nome di una funzione di formato personalizzata fornita dal parser.

Le [**funzioni FormatPropertyInstance**](formatpropertyinstance.md) e custom format restituiscono i dati formattati visualizzati nel riquadro dei dettagli dell'interfaccia Network Monitor interfaccia utente.

La figura seguente mostra come Network Monitor identifica la funzione da chiamare per ogni istanza di proprietà.

![come network monitor identifica la funzione da chiamare](images/formatprop1.png)

La procedura seguente identifica i passaggi necessari per implementare [**FormatProperties**](formatproperties.md).

**Per implementare FormatProperties**

-   Usando una struttura di ciclo, chiamare la funzione format per ogni [**struttura PROPERTYINST**](propertyinst.md) passata al parser nel parametro *lpPropInst* della [**funzione FormatProperties.**](formatproperties.md)

Di seguito è riportata un'implementazione di [**base di FormatProperties**](formatproperties.md).

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



