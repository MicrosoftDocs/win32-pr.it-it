---
description: Nella tabella seguente vengono descritte le modalità di mapping.
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: Modalità di mapping e traduzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219bfe2f587ef9bc66f53d6f08404a0448180512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226686"
---
# <a name="mapping-modes-and-translations"></a>Modalità di mapping e traduzioni

Nella tabella seguente vengono descritte le modalità di mapping.



| Modalità di mapping    | Descrizione                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MM \_ anisotropico | Ogni unità nello spazio della pagina è mappata a un'unità specificata dall'applicazione nello spazio del dispositivo. L'asse può essere ridimensionato in modo uniforme (ad esempio, un cerchio disegnato nello spazio globale potrebbe sembrare un'ellisse quando viene raffigurato in un determinato dispositivo). L'orientamento dell'asse viene inoltre specificato dall'applicazione.                  |
| \_HIENGLISH mm   | Ogni unità nello spazio della pagina è mappata a 0,001 di pollice nello spazio del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                                                 |
| \_HIMETRIC mm    | Ogni unità nello spazio della pagina è mappata a 0,01 millimetri nello spazio del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                                            |
| filtro di stato \_   | Ogni unità nello spazio della pagina è mappata a un'unità definita dall'applicazione nello spazio del dispositivo. Gli assi vengono sempre ridimensionati in modo uniforme. L'orientamento degli assi può essere specificato dall'applicazione.                                                                                                                                     |
| \_LOENGLISH mm   | Ogni unità nello spazio della pagina è mappata a 0,01 di pollice nello spazio del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                                                  |
| \_LOMETRIC mm    | Ogni unità nello spazio della pagina è mappata a 0,1 millimetri nello spazio del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                                             |
| \_testo mm        | Ogni unità nello spazio della pagina è mappata a un pixel; ovvero non viene eseguito alcun ridimensionamento. Quando non è attiva alcuna conversione (impostazione predefinita), lo spazio della pagina nella modalità di \_ mapping del testo mm è equivalente allo spazio fisico del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dall'alto verso il basso. |
| \_twip mm       | Ogni unità nello spazio pagina viene mappata a un ventesimo punto della stampante (1/1440 pollice). Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                           |



 

Per impostare una modalità di mapping, chiamare la funzione [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) . Recuperare la modalità di mapping corrente per un controller di dominio chiamando la funzione [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode) .

Le trasformazioni dello spazio della pagina per il dispositivo sono costituite da valori calcolati dai punti specificati dalla finestra e dal viewport. In questo contesto, la finestra fa riferimento al sistema di coordinate logico dello spazio della pagina, mentre il viewport fa riferimento al sistema di coordinate del dispositivo dello spazio del dispositivo. Ogni finestra e Viewport è costituito da un'origine, da un extent orizzontale ("x") e da un extent verticale ("y"). I parametri della finestra sono in coordinate logiche. viewport in coordinate del dispositivo (pixel). Il sistema combina le origini e gli extent sia dalla finestra che dal viewport per creare la trasformazione. Ciò significa che la finestra e il viewport specificano ognuno la metà dei fattori necessari per definire la trasformazione utilizzata per eseguire il mapping dei punti nello spazio della pagina allo spazio del dispositivo. Il sistema esegue quindi il mapping dell'origine della finestra all'origine del viewport e degli extent della finestra agli extent del viewport, come illustrato nella figura seguente.

![illustrazione che mostra un'origine della finestra nello spazio della pagina e un'origine del punto di vista nello spazio del dispositivo](images/cstrn-15.png)

Gli extent della finestra e del viewport stabiliscono un rapporto o un fattore di scala usato nello spazio della pagina per le trasformazioni dello spazio del dispositivo. Per le sei modalità di mapping predefinite (MM \_ HIENGLISH, mm \_ LOENGLISH, mm \_ HIMETRIC, MM \_ LOMETRIC, mm \_ Text e mm \_ twip), gli extent vengono impostati dal sistema quando viene chiamato [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) . Non possono essere modificate. Per le altre due modalità di mapping, ovvero il livello di \_ filtro e il livello di filtro mm, \_ è necessario specificare gli extent. Questa operazione viene eseguita chiamando **SetMapMode** per impostare la modalità appropriata e quindi chiamando le funzioni [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) e [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) per specificare gli extent. Nella modalità di \_ mapping del modello di filtro di tipo mm è importante chiamare **SetWindowExtEx** prima di chiamare **SetViewportExtEx**.

Le origini finestra e Viewport stabiliscono la traduzione usata nello spazio della pagina per le trasformazioni dello spazio del dispositivo. Impostare le origini della finestra e del viewport usando le funzioni [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) e [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) . Le origini sono indipendenti dagli extent e possono essere impostate da un'applicazione indipendentemente dalla modalità di mapping corrente. La modifica di una modalità di mapping non influisce sulle origini attualmente impostate (sebbene possa influire sugli extent). Le origini vengono specificate in unità assolute che non influiscono sulla modalità di mapping corrente. Per modificare le origini, usare le funzioni [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) e [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex) .

La formula seguente mostra i calcoli matematici necessari per la conversione di un punto dallo spazio della pagina allo spazio del dispositivo.

``` syntax
Dx = ((Lx - WOx) * VEx / WEx) + VOx 
```

Sono necessarie le variabili seguenti.

``` syntax
Dx     x value in device units 
Lx     x value in logical units (also known as page space units) 
WOx     window x origin 
VOx     viewport x origin 
WEx     window x-extent 
VEx     viewport x-extent 
```

La stessa equazione con y che sostituisce x trasforma il componentof y a un punto.

La formula innanzitutto compensa il punto dall'origine della coordinata. Questo valore, non più distorto dall'origine, viene quindi ridimensionato nel sistema di coordinate di destinazione in base al rapporto degli extent. Infine, il valore ridimensionato viene sottoposto a offset dall'origine di destinazione al mapping finale.

Le funzioni [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp) e [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp) possono essere usate per eseguire la conversione da punti logici a punti di dispositivo e da punti di dispositivo a punti logici rispettivamente.

 

 



