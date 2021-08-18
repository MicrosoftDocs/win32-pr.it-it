---
title: Aggiunta User-Controlled riproduzione
description: Aggiunta User-Controlled riproduzione
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- Funzione MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62d4e4af43be9877ec5bf3fae452e44ae415bc47047448cb65b64ad3446e0b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941819"
---
# <a name="adding-user-controlled-playback"></a>Aggiunta User-Controlled riproduzione

È possibile aggiungere la riproduzione controllata dall'utente a un'applicazione esistente chiamando la [**funzione MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) come indicato di seguito:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



I [**parametri MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identificano gli handle per la finestra padre e per l'istanza del modulo associata alla finestra MCIWnd. Specificano anche gli stili della finestra e il nome file (o nome del dispositivo) da associare alla finestra MCIWnd.

**MCIWndCreate** esegue automaticamente i passaggi seguenti che, per altre classi di finestra, verrebbero implementati manualmente nel codice:

1.  Registrare la classe della finestra MCIWnd.
2.  Creare la finestra MCIWnd.
3.  Caricare il contenuto specificato.
4.  Stabilire la posizione di riproduzione corrente all'inizio del contenuto.
5.  Visualizzare il controllo del dispositivo.
6.  Visualizzare l'area di riproduzione della finestra, se necessario.

 

 




