---
title: Aggiunta della riproduzione User-Controlled
description: Aggiunta della riproduzione User-Controlled
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298259"
---
# <a name="adding-user-controlled-playback"></a>Aggiunta della riproduzione User-Controlled

È possibile aggiungere la riproduzione controllata dall'utente a un'applicazione esistente chiamando la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) come segue:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



I parametri [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identificano gli handle per la finestra padre e per l'istanza del modulo associata alla finestra MCIWnd. Specificano anche gli stili della finestra e il nome del file (o il nome del dispositivo) da associare alla finestra MCIWnd.

**MCIWndCreate** esegue automaticamente i passaggi seguenti che, per le altre classi di finestra, è necessario implementare manualmente nel codice:

1.  Registrare la classe della finestra MCIWnd.
2.  Creare la finestra MCIWnd.
3.  Carica il contenuto specificato.
4.  Stabilire la posizione di riproduzione corrente all'inizio del contenuto.
5.  Visualizzare il controllo del dispositivo.
6.  Visualizzare l'area di riproduzione della finestra, se necessario.

 

 




