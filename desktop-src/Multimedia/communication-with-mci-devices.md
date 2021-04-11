---
title: Comunicazione con i dispositivi MCI
description: Comunicazione con i dispositivi MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Dispositivi MCI, comunicazione
- MCIWndGetDeviceID (macro)
- mciSendCommand (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336910"
---
# <a name="communication-with-mci-devices"></a>Comunicazione con i dispositivi MCI

Ogni dispositivo MCI può usare uno o più degli identificatori seguenti:

-   identificatore del dispositivo
-   Nome dispositivo
-   un alias
-   nome file del contenuto attualmente caricato.

MCIWnd fornisce le macro che è possibile usare per recuperare queste informazioni. È quindi possibile usare queste informazioni per comunicare tramite MCI direttamente con i dispositivi MCI associati a MCIWnd Windows.

È possibile recuperare l'identificatore del dispositivo MCI corrente usando la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) . L'identificatore del dispositivo MCI è un valore numerico che identifica l'istanza del dispositivo MCI usato dall'applicazione. L'applicazione può usare questo identificatore durante la comunicazione con un dispositivo MCI usando la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .

Per recuperare il nome del dispositivo MCI corrente, usare la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) . Il nome del dispositivo MCI è una stringa con terminazione null che identifica il tipo di dispositivo associato a una finestra MCIWnd. L'applicazione può usare questo nome durante la comunicazione con un dispositivo MCI usando **mciSendCommand**.

È possibile recuperare l'alias del dispositivo MCI corrente usando la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) . L'applicazione può usare questo alias durante la comunicazione con un dispositivo MCI usando la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .

Infine, è possibile recuperare il nome file usato da un dispositivo MCI usando la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) . Il nome file identifica il contenuto attualmente associato a una finestra MCIWnd. L'applicazione può usare questo nome file durante la comunicazione con un dispositivo MCI usando **mciSendCommand** o **mciSendString**.

 

 