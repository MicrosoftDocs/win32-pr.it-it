---
description: La penna, il pennello, la bitmap, la tavolozza, l'area e il tracciato associati a un controller di dominio sono definiti oggetti grafici. Gli attributi seguenti sono associati a ognuno di questi oggetti.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Oggetti grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf256cd8eafd6ee346c12f6658a7c3dd388c94fb4107b010528e47c126fce2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831961"
---
# <a name="graphic-objects"></a>Oggetti grafici

La penna, il pennello, la bitmap, la tavolozza, l'area e il tracciato associati a un controller di dominio sono definiti oggetti grafici. Gli attributi seguenti sono associati a ognuno di questi oggetti.



| Oggetto grafico | Attributi associati                                                               |
|----------------|-------------------------------------------------------------------------------------|
| Bitmap         | Dimensioni, in byte. dimensioni, in pixel; formato colore; schema di compressione; E così via. |
| Brush          | Stile, colore, motivo e origine.                                                  |
| Tavolozza        | Colori e dimensioni (o numero di colori).                                              |
| Carattere           | Nome del carattere tipografico, larghezza, altezza, peso, set di caratteri e così via.                     |
| Percorso           | Forma.                                                                              |
| Penna            | Stile, larghezza e colore.                                                            |
| Region         | Posizione e dimensioni.                                                            |



 

Quando un'applicazione crea un controller di dominio, il sistema archivia automaticamente un set di oggetti predefiniti (non è presente alcuna bitmap o percorso predefinito). Un'applicazione può esaminare gli attributi degli oggetti predefiniti chiamando le [**funzioni GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) [**e GetObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) L'applicazione può modificare queste impostazioni predefinite creando un nuovo oggetto e selezionandolo nel controller di dominio. Un oggetto viene selezionato in un controller di dominio chiamando la [**funzione SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)

Un'applicazione può impostare il colore del pennello corrente su un valore di colore specificato [**con SetDCBrushColor.**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)

La [**funzione GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) restituisce il colore del pennello DC. La [**funzione SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) imposta il colore della penna su un valore di colore specificato. La [**funzione GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) restituisce il colore della penna DC.

 

 



