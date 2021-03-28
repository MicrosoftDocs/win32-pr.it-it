---
description: Le penne, i pennelli, le bitmap, le tavolozze, le aree e i percorsi associati a un controller di dominio sono detti oggetti grafici. Gli attributi seguenti sono associati a ognuno di questi oggetti.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Oggetti grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993984"
---
# <a name="graphic-objects"></a>Oggetti grafici

Le penne, i pennelli, le bitmap, le tavolozze, le aree e i percorsi associati a un controller di dominio sono detti oggetti grafici. Gli attributi seguenti sono associati a ognuno di questi oggetti.



| Oggetto grafico | Attributi associati                                                               |
|----------------|-------------------------------------------------------------------------------------|
| Bitmap         | Dimensioni, in byte; dimensioni, in pixel; formato colore; schema di compressione; E così via. |
| Brush          | Stile, colore, motivo e origine.                                                  |
| Tavolozza        | Colori e dimensioni (o numero di colori).                                              |
| Carattere           | Nome tipografico, larghezza, altezza, peso, set di caratteri e così via.                     |
| Percorso           | Forma.                                                                              |
| Penna            | Stile, larghezza e colore.                                                            |
| Region         | Posizione e dimensioni.                                                            |



 

Quando un'applicazione crea un controller di dominio, il sistema archivia automaticamente un set di oggetti predefiniti (non esiste alcuna bitmap o percorso predefinito). Un'applicazione può esaminare gli attributi degli oggetti predefiniti chiamando le funzioni [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . L'applicazione può modificare queste impostazioni predefinite creando un nuovo oggetto e selezionandolo nel controller di dominio. Un oggetto viene selezionato in un controller di dominio chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .

Un'applicazione può impostare il colore corrente del pennello su un valore di colore specificato con [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).

La funzione [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) restituisce il colore del pennello del controller di dominio. La funzione [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) imposta il colore della penna su un valore di colore specificato. La funzione [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) restituisce il colore della penna del controller di dominio.

 

 



