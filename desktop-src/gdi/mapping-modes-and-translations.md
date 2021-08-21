---
description: Le modalità di mapping sono descritte nella tabella seguente.
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: Modalità di mapping e traduzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242ba699a8ec7289495cbcdff33e940460b20bcabffa373d5c792b1aee0fe9d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760147"
---
# <a name="mapping-modes-and-translations"></a>Modalità di mapping e traduzioni

Le modalità di mapping sono descritte nella tabella seguente.



| Modalità di mapping    | Descrizione                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MM \_ ANISOTROP | Ogni unità nello spazio della pagina viene mappata a un'unità specificata dall'applicazione nello spazio del dispositivo. L'asse può o meno essere ridimensionato in modo uniforme(ad esempio, un cerchio disegnato nello spazio globale può sembrare un'ellisse quando viene rappresentato in un determinato dispositivo). Anche l'orientamento dell'asse viene specificato dall'applicazione.                  |
| MM \_ HIENGLISH   | Ogni unità nello spazio della pagina viene mappata a 0,001 pollici nello spazio del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                                                 |
| MM \_ HIMETRIC    | Ogni unità nello spazio della pagina viene mappata a 0,01 millimetri nello spazio del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                                            |
| MM \_ ISOTROP   | Ogni unità nello spazio della pagina viene mappata a un'unità definita dall'applicazione nello spazio del dispositivo. Gli assi vengono sempre ridimensionati in modo uniforme. L'orientamento degli assi può essere specificato dall'applicazione.                                                                                                                                     |
| MM \_ LOENGLISH   | Ogni unità nello spazio della pagina viene mappata a 0,01 pollici nello spazio del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                                                  |
| MM \_ LOMETRIC    | Ogni unità nello spazio della pagina viene mappata a 0,1 millimetri nello spazio del dispositivo. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                                             |
| TESTO \_ MM        | Ogni unità nello spazio della pagina viene mappata a un pixel; ciò significa che non viene eseguito alcun ridimensionamento. Quando non è attiva alcuna traduzione (impostazione predefinita), lo spazio della pagina nella modalità di mapping TESTO MM \_ equivale allo spazio del dispositivo fisico. Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dall'alto verso il basso. |
| MM \_ TWIPS       | Ogni unità nello spazio della pagina viene mappata a un ventesimo del punto di una stampante (1/1440 pollici). Il valore di x aumenta da sinistra a destra. Il valore di y aumenta dal basso verso l'alto.                                                                                                                                           |



 

Per impostare una modalità di mapping, chiamare la [**funzione SetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) Recuperare la modalità di mapping corrente per un controller di dominio chiamando la [**funzione GetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)

Le trasformazioni da spazio di pagina a spazio dispositivo sono costituite da valori calcolati dai punti specificati dalla finestra e dal viewport. In questo contesto, la finestra fa riferimento al sistema di coordinate logico dello spazio della pagina, mentre il viewport fa riferimento al sistema di coordinate del dispositivo dello spazio del dispositivo. La finestra e il viewport sono costituiti da un'origine, un extent orizzontale ("x") e un extent verticale ("y"). I parametri della finestra sono in coordinate logiche. il viewport nelle coordinate del dispositivo (pixel). Il sistema combina le origini e gli extent sia dalla finestra che dal viewport per creare la trasformazione. Ciò significa che la finestra e il viewport specificano ognuno la metà dei fattori necessari per definire la trasformazione usata per eseguire il mapping dei punti nello spazio della pagina allo spazio del dispositivo. Di conseguenza, il sistema esegue il mapping dell'origine della finestra all'origine del viewport e degli extent della finestra agli extent del viewport, come illustrato nella figura seguente.

![Figura che mostra l'origine di una finestra nello spazio della pagina e un'origine del punto di vista nello spazio del dispositivo](images/cstrn-15.png)

Gli extent della finestra e del viewport stabiliscono un rapporto o un fattore di scala usato nelle trasformazioni dello spazio della pagina e dello spazio del dispositivo. Per le sei modalità di mapping predefinite (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM LOMETRIC, MM TEXT e MM TWIPS), gli extent vengono impostati dal sistema quando viene chiamato \_ \_ \_ [**SetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) Non possono essere modificati. Le altre due modalità di mapping (MM \_ ISOTROP e MM \_ ANISOTROP) richiedono che gli extent siano specificati. Questa operazione viene eseguita chiamando **SetMapMode** per impostare la modalità appropriata e quindi chiamando le [**funzioni SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) e [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) per specificare gli extent. Nella modalità \_ di mapping MM ISOTROP è importante chiamare **SetWindowExtEx** prima di **chiamare SetViewportExtEx**.

Le origini della finestra e del viewport stabiliscono la traduzione usata nello spazio della pagina per le trasformazioni dello spazio del dispositivo. Impostare le origini della finestra e del viewport usando le [**funzioni SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) [**e SetViewportOrgEx.**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) Le origini sono indipendenti dalle estensioni e un'applicazione può impostarle indipendentemente dalla modalità di mapping corrente. La modifica di una modalità di mapping non influisce sulle origini attualmente impostate( anche se può influire sugli extent). Le origini vengono specificate in unità assolute non influenzate dalla modalità di mapping corrente. Per modificare le origini, usare le [**funzioni OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) e [**OffsetViewportOrgEx.**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)

La formula seguente illustra i calcoli matematici coinvolti nella conversione di un punto dallo spazio della pagina allo spazio del dispositivo.

``` syntax
Dx = ((Lx - WOx) * VEx / WEx) + VOx 
```

Sono coinvolte le variabili seguenti.

``` syntax
Dx     x value in device units 
Lx     x value in logical units (also known as page space units) 
WOx     window x origin 
VOx     viewport x origin 
WEx     window x-extent 
VEx     viewport x-extent 
```

La stessa equazione con y che sostituisce x trasforma il componente y di un punto.

La formula innanzitutto scosta il punto dall'origine delle coordinate. Questo valore, non più distorto dall'origine, viene quindi ridimensionato nel sistema di coordinate di destinazione in base al rapporto degli extent. Infine, il valore ridimensionato viene compensato dall'origine di destinazione al mapping finale.

Le [**funzioni LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp) e [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp) possono essere usate rispettivamente per eseguire la conversione da punti logici a punti dispositivo e da punti dispositivo a punti logici.

 

 



