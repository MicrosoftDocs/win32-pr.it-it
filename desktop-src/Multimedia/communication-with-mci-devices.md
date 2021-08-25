---
title: Comunicazione con i dispositivi MCI
description: Comunicazione con i dispositivi MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- dispositivi MCI, comunicazione
- Macro MCIWndGetDeviceID
- MciSendCommand - funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd04187b948adf144a317a1d9eab80efb60bab8e7b05eaccffeb34722baa98a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785906"
---
# <a name="communication-with-mci-devices"></a>Comunicazione con i dispositivi MCI

È possibile che ogni dispositivo MCI usi uno o più degli identificatori seguenti:

-   un identificatore di dispositivo
-   un nome di dispositivo
-   un alias
-   nome del file del contenuto attualmente caricato.

MCIWnd fornisce macro che è possibile usare per recuperare queste informazioni. È quindi possibile usare queste informazioni per comunicare tramite MCI direttamente con i dispositivi MCI associati alle finestre MCIWnd.

È possibile recuperare l'identificatore del dispositivo MCI corrente usando la macro [**MCIWndGetDeviceID.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) L'identificatore del dispositivo MCI è un valore numerico che identifica l'istanza del dispositivo MCI in uso nell'applicazione. L'applicazione può usare questo identificatore durante la comunicazione con un dispositivo MCI usando la [**funzione mciSendCommand.**](/previous-versions//dd757160(v=vs.85))

Per recuperare il nome del dispositivo MCI corrente, usare la macro [**MCIWndGetDevice.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) Il nome del dispositivo MCI è una stringa con terminazione Null che identifica il tipo di dispositivo associato a una finestra MCIWnd. L'applicazione può usare questo nome durante la comunicazione con un dispositivo MCI usando **mciSendCommand**.

È possibile recuperare l'alias del dispositivo MCI corrente usando la macro [**MCIWndGetAlias.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) L'applicazione può usare questo alias durante la comunicazione con un dispositivo MCI usando la [**funzione mciSendString.**](/previous-versions//dd757161(v=vs.85))

Infine, è possibile recuperare il nome file usato da un dispositivo MCI usando la macro [**MCIWndGetFileName.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) Il nome del file identifica il contenuto attualmente associato a una finestra MCIWnd. L'applicazione può usare questo nome file durante la comunicazione con un dispositivo MCI usando **mciSendCommand** o **mciSendString.**

 

 