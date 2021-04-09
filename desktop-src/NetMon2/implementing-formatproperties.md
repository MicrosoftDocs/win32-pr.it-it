---
description: Network Monitor chiama la funzione FormatProperties per formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementazione di FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128914"
---
# <a name="implementing-formatproperties"></a>Implementazione di FormatProperties

Network Monitor chiama la funzione [**FormatProperties**](formatproperties.md) per formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor. In genere, **FormatProperties** viene chiamato per formattare la riga di riepilogo per un protocollo e quindi per formattare tutte le istanze di proprietà del protocollo all'interno di un frame. Tuttavia, Network Monitor non identifica il numero di volte in cui viene chiamato **FormatProperties** per un parser specifico.

Quando si chiama [**FormatProperties**](formatproperties.md), Network Monitor fornisce una struttura [**PROPERTYINST**](propertyinst.md) per ogni proprietà visualizzata. La struttura **PROPERTYINST** fornisce informazioni sui dati da visualizzare, incluso un puntatore alla struttura [**PROPERTYINFO**](propertyinfo.md) che specifica la funzione da utilizzare per formattare la proprietà dei dati visualizzati.

> [!Note]  
> Quando si aggiunge una proprietà al [*database della proprietà*](p.md) del parser, viene specificata una struttura [**PROPERTYINFO**](propertyinfo.md) .

 

Network Monitor identifica la funzione Format da chiamare per ogni istanza della proprietà. Il membro **InstanceData** della struttura [**PROPERTYINFO**](propertyinfo.md) può specificare gli elementi seguenti:

-   Funzione [**FormatPropertyInstance**](formatpropertyinstance.md) per utilizzare il [*formattatore generico*](g.md) fornito da Network Monitor.

    - oppure -

-   Nome di una funzione di formato personalizzata fornita dal parser.

Le funzioni [**FormatPropertyInstance**](formatpropertyinstance.md) e Format personalizzato restituiscono i dati formattati che vengono visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.

Nella figura seguente viene illustrato il modo in cui Network Monitor identifica la funzione da chiamare per ogni istanza della proprietà.

![modalità di identificazione della funzione da chiamare in Network Monitor](images/formatprop1.png)

Nella procedura seguente vengono identificati i passaggi necessari per implementare [**FormatProperties**](formatproperties.md).

**Per implementare FormatProperties**

-   Utilizzando una struttura di ciclo, chiamare la funzione Format per ogni struttura [**PROPERTYINST**](propertyinst.md) passata al parser nel parametro *LpPropInst* della funzione [**FormatProperties**](formatproperties.md) .

Di seguito è riportata un'implementazione di base di [**FormatProperties**](formatproperties.md).

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

 

 



