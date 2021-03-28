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
# <a name="hmonitor-and-the-device-context"></a><span data-ttu-id="5d5d9-103">HMONITOR e il contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="5d5d9-103">HMONITOR and the Device Context</span></span>

<span data-ttu-id="5d5d9-104">Ogni schermo fisico è rappresentato da un handle di monitoraggio di tipo **HMONITOR**.</span><span class="sxs-lookup"><span data-stu-id="5d5d9-104">Each physical display is represented by a monitor handle of type **HMONITOR**.</span></span> <span data-ttu-id="5d5d9-105">Un **HMONITOR** valido è sicuramente non null.</span><span class="sxs-lookup"><span data-stu-id="5d5d9-105">A valid **HMONITOR** is guaranteed to be non-NULL.</span></span> <span data-ttu-id="5d5d9-106">Una visualizzazione fisica ha lo stesso **HMONITOR** purché faccia parte del desktop.</span><span class="sxs-lookup"><span data-stu-id="5d5d9-106">A physical display has the same **HMONITOR** as long as it is part of the desktop.</span></span> <span data-ttu-id="5d5d9-107">Quando viene inviato un messaggio **WM \_ DISPLAYCHANGE** , è possibile che qualsiasi monitoraggio venga rimosso dal desktop, quindi il relativo **HMONITOR** diventa non valido o le impostazioni modificate.</span><span class="sxs-lookup"><span data-stu-id="5d5d9-107">When a **WM\_DISPLAYCHANGE** message is sent, any monitor may be removed from the desktop and thus its **HMONITOR** becomes invalid or has its settings changed.</span></span> <span data-ttu-id="5d5d9-108">Pertanto, un'applicazione deve verificare se tutti **HMONITORS** sono validi quando viene inviato questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="5d5d9-108">Therefore, an application should check whether all **HMONITORS** are valid when this message is sent.</span></span>

<span data-ttu-id="5d5d9-109">Tutte le funzioni che restituiscono un contesto di periferica di visualizzazione (DC) normalmente restituiscono un controller di dominio per il monitor primario.</span><span class="sxs-lookup"><span data-stu-id="5d5d9-109">Any function that returns a display device context (DC) normally returns a DC for the primary monitor.</span></span> <span data-ttu-id="5d5d9-110">Per ottenere il controller di dominio per un altro monitor, utilizzare la funzione [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="5d5d9-110">To obtain the DC for another monitor, use the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span> <span data-ttu-id="5d5d9-111">In alternativa, è possibile usare il nome del dispositivo della funzione [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) per creare un controller di dominio con [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="5d5d9-111">Or, you can use the device name from the [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) function to create a DC with [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="5d5d9-112">Tuttavia, se la funzione, ad esempio [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), ottiene un controller di dominio per una finestra che si estende su più di una visualizzazione, il controller di dominio estenderà anche le due visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="5d5d9-112">However, if the function, such as [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), gets a DC for a window that spans more than one display, the DC will also span the two displays.</span></span>

 

 



