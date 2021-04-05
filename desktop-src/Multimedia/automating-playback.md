---
title: Automazione della riproduzione
description: Automazione della riproduzione
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate (macro)
- MCIWndPlay (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714074"
---
# <a name="automating-playback"></a>Automazione della riproduzione

È possibile automatizzare la riproduzione nell'applicazione usando [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , insieme alla macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) . Per automatizzare la riproduzione, specificare gli \_ stili MCIWNDF NOPLAYBAR e MCIWNDF \_ NOTIFYMODE nel parametro **MCIWndCreate * * * dwStyle* . Specificare lo \_ stile di NOPLAYBAR MCIWNDF per nascondere la barra degli strumenti e lo \_ stile di NOTIFYMODE MCIWNDF per emettere un messaggio di notifica appropriato quando il dispositivo smette di riprodursi.

È possibile riprodurre il dispositivo o il file specificato in **MCIWndCreate** usando **MCIWndPlay**. La macro MCIWndPlay inizia a riprodurre il contenuto dalla posizione di riproduzione corrente e continua fino alla fine.

È possibile eliminare o chiudere una finestra MCIWnd usando la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) o [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) . La macro **MCIWndDestroy** chiude il dispositivo o il file ed elimina la finestra MCIWnd invalidando il relativo handle. Se l'applicazione può riutilizzare la finestra MCIWnd, utilizzare **MCIWndClose** per chiudere il dispositivo senza eliminare definitivamente la finestra.

L'applicazione può rilevare quando il dispositivo smette di essere riprodotto e chiude automaticamente la finestra. A tale scopo, specificare lo \_ stile NOTIFYMODE MCIWNDF per il parametro *DwStyle* di [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea). In questo modo, il dispositivo invia un messaggio [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) ogni volta che modifica le modalità. L'applicazione può intercettare questo messaggio per determinare se la riproduzione del dispositivo è stata interrotta. Quando il dispositivo smette di rigiocare, l'applicazione chiude la finestra.

 

 




