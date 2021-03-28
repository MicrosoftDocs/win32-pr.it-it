---
description: Ogni schermo fisico è rappresentato da un handle di monitoraggio di tipo HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR e il contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993981"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR e il contesto di dispositivo

Ogni schermo fisico è rappresentato da un handle di monitoraggio di tipo **HMONITOR**. Un **HMONITOR** valido è sicuramente non null. Una visualizzazione fisica ha lo stesso **HMONITOR** purché faccia parte del desktop. Quando viene inviato un messaggio **WM \_ DISPLAYCHANGE** , è possibile che qualsiasi monitoraggio venga rimosso dal desktop, quindi il relativo **HMONITOR** diventa non valido o le impostazioni modificate. Pertanto, un'applicazione deve verificare se tutti **HMONITORS** sono validi quando viene inviato questo messaggio.

Tutte le funzioni che restituiscono un contesto di periferica di visualizzazione (DC) normalmente restituiscono un controller di dominio per il monitor primario. Per ottenere il controller di dominio per un altro monitor, utilizzare la funzione [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) . In alternativa, è possibile usare il nome del dispositivo della funzione [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) per creare un controller di dominio con [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca). Tuttavia, se la funzione, ad esempio [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), ottiene un controller di dominio per una finestra che si estende su più di una visualizzazione, il controller di dominio estenderà anche le due visualizzazioni.

 

 



