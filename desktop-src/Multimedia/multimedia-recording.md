---
title: Registrazione multimediale
description: Registrazione multimediale
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- McIWndCreate - funzione
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b10c1d557566090343a71f760ab249093077491a1e9d1fb570dd5e97fc1f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985204"
---
# <a name="multimedia-recording"></a>Registrazione multimediale

È possibile implementare funzionalità di registrazione nell'applicazione usando l'interfaccia utente incorporata in MCIWnd. È possibile usare la [**funzione MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) per fornire controlli per l'avvio e l'arresto della registrazione e per il salvataggio delle informazioni registrate. Con **MCIWndCreate** è possibile specificare gli stili della finestra per visualizzare una finestra MCIWnd e includere il **pulsante Registra** sulla barra degli strumenti. Usando **MCIWndNew,** è possibile specificare il tipo di dispositivo registrato e specificare che le informazioni devono essere acquisite in un nuovo file.

Se l'applicazione richiede una maggiore sofisticazione, è possibile automatizzare e personalizzare la registrazione usando la macro [**MCIWndRecord.**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) Per altre informazioni, vedere [Personalizzazione del processo di registrazione.](customizing-the-recording-process.md)

> [!Note]  
> Alcuni dispositivi, ad esempio l'audio CD e MCIAVI, vengono usati solo per la riproduzione. Per la registrazione è possibile usare altri dispositivi, ad esempio dispositivi audio waveform. Se si specifica un dispositivo che non può registrare, MCIWnd omette il **pulsante Registra** sulla barra degli strumenti.

 

 

 




