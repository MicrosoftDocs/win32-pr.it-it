---
title: Fornire aggiornamenti sullo stato
description: Fornire aggiornamenti sullo stato
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- MCIWndSetActiveTimer (macro)
- MCIWndSetInactiveTimer (macro)
- MCIWndGetActiveTimer (macro)
- MCIWndGetInactiveTimer (macro)
- MCIWndSetTimers (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395826"
---
# <a name="providing-status-updates"></a>Fornire aggiornamenti sullo stato

MCIWnd usa i timer per aggiornare periodicamente le informazioni nella barra del titolo della finestra e nella barra di scorrimento e per inviare messaggi di notifica alla finestra padre. Un timer controlla il periodo di aggiornamento della finestra MCIWnd attiva e un secondo timer controlla il periodo di aggiornamento per le finestre MCIWnd che sono inattive. L'applicazione può utilizzare le macro del timer MCIWnd per recuperare le impostazioni correnti del timer e per modificare i periodi di aggiornamento.

È possibile impostare il periodo di aggiornamento utilizzato dal timer della finestra attiva utilizzando la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) . Questa macro imposta il periodo usato da MCIWnd per aggiornare il controllo TrackBar, per aggiornare la posizione di riproduzione indicata nella barra del titolo della finestra e per notificare alla finestra padre che il supporto è stato modificato. È possibile recuperare il periodo di aggiornamento corrente utilizzato dal timer della finestra attiva utilizzando la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) . Il periodo di aggiornamento predefinito per il timer della finestra attiva è pari a 500 millisecondi.

È possibile impostare il periodo di aggiornamento utilizzato dal timer della finestra inattiva utilizzando la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) . Questa macro imposta il periodo usato da MCIWnd per aggiornare il controllo TrackBar, per aggiornare la posizione di riproduzione indicata nella didascalia della finestra e per notificare alla finestra padre che il supporto è stato modificato. È possibile recuperare il periodo di aggiornamento corrente utilizzato dal timer della finestra inattiva utilizzando la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) . Il periodo di aggiornamento predefinito per il timer della finestra inattiva è pari a 2000 millisecondi.

L'applicazione può impostare contemporaneamente il periodo di aggiornamento per entrambi i timer usando la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) . Lo spazio di archiviazione per il valore del periodo di aggiornamento è limitato a 16 bit. Se è necessaria una quantità maggiore per uno dei due periodi di aggiornamento, impostare i timer singolarmente.

 

 




