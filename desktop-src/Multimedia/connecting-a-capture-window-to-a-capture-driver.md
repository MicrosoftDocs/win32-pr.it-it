---
title: Connessione di una finestra di acquisizione a un driver di acquisizione
description: Connessione di una finestra di acquisizione a un driver di acquisizione
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- Messaggio WM_CAP_DRIVER_CONNECT
- capDriverConnect (macro)
- capGetDriverDescription (funzione)
- Messaggio WM_CAP_DRIVER_GET_NAME
- capDriverGetName (macro)
- Messaggio WM_CAP_DRIVER_GET_VERSION
- capDriverGetVersion (macro)
- Messaggio WM_CAP_DRIVER_DISCONNECT
- capDriverDisconnect (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710156"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Connessione di una finestra di acquisizione a un driver di acquisizione

È possibile connettere o disconnettere dinamicamente una finestra di acquisizione a un driver di acquisizione. È possibile connettere o associare una finestra di acquisizione a un driver di acquisizione usando il messaggio di [**\_ \_ \_ connessione driver WM Cap**](wm-cap-driver-connect.md) (o la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ). Dopo la connessione di una finestra di acquisizione e di un driver di acquisizione, è possibile inviare messaggi specifici del dispositivo al driver di acquisizione associato a una finestra di acquisizione.

Se si dispone di più di un dispositivo di acquisizione installato in un sistema, è possibile connettere una finestra di acquisizione a un driver di dispositivo di acquisizione video specifico specificando un numero intero per il parametro *wParam* del \_ messaggio di \_ connessione driver WM Cap \_ . Il valore integer è un indice che identifica un driver di acquisizione video elencato nel registro di sistema o nella \[ \] sezione driver del file SYSTEM.INI. Usare zero per la prima voce di indice.

È possibile recuperare il nome e la versione di un driver di acquisizione installato utilizzando la funzione [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) . L'applicazione può usare questa funzione per enumerare i driver e i dispositivi di acquisizione installati, in modo che l'utente possa selezionare un dispositivo di acquisizione per connettersi a una finestra di acquisizione.

È possibile recuperare il nome del driver di dispositivo di acquisizione connesso a una finestra di acquisizione usando [**il \_ driver di WM Cap \_ \_ get \_ Name**](wm-cap-driver-get-name.md) Message (o la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ). Per recuperare la versione di un driver di acquisizione installato, usare il messaggio [**WM \_ Cap \_ driver \_ get \_ Version**](wm-cap-driver-get-version.md) (o la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).

È possibile disconnettere una finestra di acquisizione da un driver di acquisizione usando il messaggio di [**\_ \_ \_ disconnessione del driver WM Cap**](wm-cap-driver-disconnect.md) (o la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).

Quando viene eliminata definitivamente una finestra di acquisizione, i driver di dispositivo di acquisizione video connessi vengono automaticamente disconnessi.

 

 




