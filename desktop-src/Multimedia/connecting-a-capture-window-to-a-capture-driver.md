---
title: Connessione di una finestra di acquisizione a un driver di acquisizione
description: Connessione di una finestra di acquisizione a un driver di acquisizione
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT messaggio
- Macro capDriverConnect
- Funzione capGetDriverDescription
- WM_CAP_DRIVER_GET_NAME messaggio
- Macro capDriverGetName
- WM_CAP_DRIVER_GET_VERSION messaggio
- Macro capDriverGetVersion
- WM_CAP_DRIVER_DISCONNECT messaggio
- Macro capDriverDisconnect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf74b5dc7cda0fdb73c8f9bd73f61de5ecefc157c20816c110d71e04bba6c196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144904"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Connessione di una finestra di acquisizione a un driver di acquisizione

È possibile connettere o disconnettere dinamicamente una finestra di acquisizione a un driver di acquisizione. È possibile connettere o associare una finestra di acquisizione a un driver di acquisizione usando il messaggio [**WM \_ CAP DRIVER \_ \_ CONNECT**](wm-cap-driver-connect.md) (o la macro [**capDriverConnect).**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) Dopo aver connesso una finestra di acquisizione e un driver di acquisizione, è possibile inviare messaggi specifici del dispositivo al driver di acquisizione associato a una finestra di acquisizione.

Se in un sistema sono installati più dispositivi di acquisizione, è possibile connettere una finestra di acquisizione a un driver di dispositivo di acquisizione video specifico specificando un numero intero per il *parametro wParam* del messaggio WM \_ CAP DRIVER \_ \_ CONNECT. Il numero intero è un indice che identifica un driver di acquisizione video elencato nel Registro di sistema o nella sezione \[ drivers \] del file SYSTEM.INI. Usare zero per la prima voce di indice.

È possibile recuperare il nome e la versione di un driver di acquisizione installato usando la [**funzione capGetDriverDescription.**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) L'applicazione può usare questa funzione per enumerare i driver e i dispositivi di acquisizione installati, in modo che l'utente possa selezionare un dispositivo di acquisizione per connettersi a una finestra di acquisizione.

È possibile recuperare il nome del driver di dispositivo di acquisizione connesso a una finestra di acquisizione usando il messaggio [**WM CAP DRIVER GET \_ \_ \_ \_ NAME**](wm-cap-driver-get-name.md) (o la macro [**capDriverGetName).**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) Per recuperare la versione di un driver di acquisizione installato, usare il messaggio [**GET \_ \_ \_ \_ VERSION**](wm-cap-driver-get-version.md) del DRIVER CAP WM (o la macro [**capDriverGetVersion).**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion)

È possibile disconnettere una finestra di acquisizione da un driver di acquisizione usando il messaggio [**WM \_ CAP DRIVER \_ \_ DISCONNECT**](wm-cap-driver-disconnect.md) (o la macro [**capDriverDisconnect).**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect)

Quando una finestra di acquisizione viene distrutta, tutti i driver di dispositivo di acquisizione video connessi vengono disconnessi automaticamente.

 

 




