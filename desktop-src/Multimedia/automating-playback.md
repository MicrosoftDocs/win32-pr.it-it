---
title: Automazione della riproduzione
description: Automazione della riproduzione
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- Macro MCIWndCreate
- Macro MCIWndPlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1c05041bade08f47505a2cf1207739777c5af825ea9f5f300b343b87efe3c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691971"
---
# <a name="automating-playback"></a>Automazione della riproduzione

È possibile automatizzare la riproduzione nell'applicazione usando [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e la macro [**MCIWndPlay,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) insieme alla macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose.**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) Per automatizzare la riproduzione, specificare gli stili MCIWNDF \_ NOPLAYBAR e MCIWNDF \_ NOTIFYMODE nel **parametro MCIWndCreate**_dwStyle._ Specificare lo stile MCIWNDF NOPLAYBAR per nascondere la barra degli strumenti e lo stile NOTIFYMODE MCIWNDF per inviare un messaggio di notifica appropriato quando il \_ dispositivo smette di essere \_ riprodotto.

È possibile riprodurre il dispositivo o il file specificato in **MCIWndCreate** usando **MCIWndPlay.** La macro MCIWndPlay inizia a riprodurre il contenuto dalla posizione di riproduzione corrente e continua fino alla fine.

È possibile eliminare o chiudere una finestra MCIWnd usando la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose.**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) La macro **MCIWndDestroy** chiude il dispositivo o il file ed elimina la finestra MCIWnd invalidando l'handle. Se l'applicazione può riutilizzare la finestra **MCIWnd, usare MCIWndClose** per chiudere il dispositivo senza eliminare la finestra.

L'applicazione può rilevare quando il dispositivo smette di riprodurre e chiudere automaticamente la finestra. A tale scopo, specificare lo stile NOTIFYMODE MCIWNDF per \_ il *parametro dwStyle* di [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea). In questo modo il dispositivo invia un [**messaggio \_ NOTIFYMODE MCIWNDM**](mciwndm-notifymode.md) ogni volta che cambia modalità. L'applicazione può intercettare questo messaggio per determinare se la riproduzione del dispositivo è stata interrotta. Quando il dispositivo smette di essere riprodotto, l'applicazione chiude la finestra.

 

 




