---
description: Ogni visualizzazione fisica è rappresentata da un handle di monitoraggio di tipo HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR e contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb727457c388710b19d8f22bef8f65d76e9d8c5c27b0ec7dfcbf55a4acea3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558751"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR e contesto di dispositivo

Ogni visualizzazione fisica è rappresentata da un handle di monitoraggio di **tipo HMONITOR.** È **garantito che un HMONITOR** valido sia diverso da NULL. Uno schermo fisico ha lo stesso **HMONITOR** purché sia parte del desktop. Quando viene inviato un messaggio **WM \_ DISPLAYCHANGE,** qualsiasi monitoraggio può essere rimosso dal desktop e pertanto il relativo **HMONITOR** non è più valido o le impostazioni sono state modificate. Pertanto, un'applicazione deve controllare se tutti **gli HMONITOR sono** validi quando viene inviato questo messaggio.

Qualsiasi funzione che restituisce un contesto di dispositivo di visualizzazione restituisce in genere un controller di dominio per il monitoraggio primario. Per ottenere il controller di dominio per un altro monitoraggio, usare la [**funzione EnumDisplayMonitors.**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) In caso contrario, è possibile usare il nome del dispositivo dalla [**funzione GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) per creare un controller di dominio con [**CreateDC.**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) Tuttavia, se la funzione, ad esempio [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), ottiene un controller di dominio per una finestra che si estende su più di uno schermo, il controller di dominio estenderà anche i due schermi.

 

 



