---
description: Quando si usano più monitor come visualizzazioni indipendenti, il desktop contiene una visualizzazione o un set di visualizzazioni.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Uso di più monitor come visualizzazioni indipendenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980506"
---
# <a name="using-multiple-monitors-as-independent-displays"></a><span data-ttu-id="f714f-103">Uso di più monitor come visualizzazioni indipendenti</span><span class="sxs-lookup"><span data-stu-id="f714f-103">Using Multiple Monitors as Independent Displays</span></span>

<span data-ttu-id="f714f-104">Quando si usano più monitor come visualizzazioni indipendenti, il desktop contiene una visualizzazione o un set di visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f714f-104">When using multiple monitors as independent displays, the desktop contains one display or set of displays.</span></span> <span data-ttu-id="f714f-105">Questo set di visualizzazioni include sempre il monitoraggio primario e si comporta come indicato nelle altre sezioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f714f-105">This set of displays always includes the primary monitor and behaves as mentioned in the other sections of this topic.</span></span> <span data-ttu-id="f714f-106">Un'applicazione può utilizzare qualsiasi altro monitor come display indipendente.</span><span class="sxs-lookup"><span data-stu-id="f714f-106">An application can use any other monitor as an independent display.</span></span>

> [!Note]  
> <span data-ttu-id="f714f-107">L'utilizzo di altri monitoraggi come visualizzazioni indipendenti non è supportato nei driver implementati per Windows Display Driver Model (WDDM).</span><span class="sxs-lookup"><span data-stu-id="f714f-107">Using other monitors as independent displays isn't supported on drivers that are implemented to the Windows Display Driver Model (WDDM).</span></span>

 

<span data-ttu-id="f714f-108">Windows Manager non è in grado di riconoscere le visualizzazioni indipendenti.</span><span class="sxs-lookup"><span data-stu-id="f714f-108">The window manager knows nothing about the independent displays.</span></span> <span data-ttu-id="f714f-109">Sono completamente controllati dall'applicazione e non sono disponibili funzioni di gestione finestre per l'applicazione. tutte le chiamate di Window Manager passano automaticamente alla visualizzazione principale.</span><span class="sxs-lookup"><span data-stu-id="f714f-109">They are completely controlled by the application, and no window manager functions are available to the application (all window manager calls automatically go to the primary display).</span></span> <span data-ttu-id="f714f-110">Ogni visualizzazione indipendente ha una propria origine e coordinate orizzontali e verticali ed è accessibile tramite le funzioni GDI, ad esempio [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) , o le funzioni DirectX, ad esempio **DirectDrawCreate**.</span><span class="sxs-lookup"><span data-stu-id="f714f-110">Each independent display has its own origin and horizontal and vertical coordinates, and is accessed through the GDI functions such as [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) or the DirectX functions such as **DirectDrawCreate**.</span></span>

<span data-ttu-id="f714f-111">Per individuare gli schermi indipendenti, chiamare [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e cercare le visualizzazioni che non dispongono \_ di un dispositivo \_ di visualizzazione collegato \_ al flag del \_ desktop nella struttura del [**\_ dispositivo di visualizzazione**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="f714f-111">To locate the independent displays, call [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and look for the displays that do not have DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span>

<span data-ttu-id="f714f-112">Un'applicazione può aprire una visualizzazione chiamando</span><span class="sxs-lookup"><span data-stu-id="f714f-112">An application can open a display by calling</span></span>


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



<span data-ttu-id="f714f-113">In questa chiamata il parametro *lpszDisplayName* è uno dei nomi di dispositivo restituiti da [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e *lpDevMode* è una descrizione della modalità grafica per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f714f-113">In this call, the *lpszDisplayName* parameter is one of the device names returned by [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and *lpDevMode* is a description of the graphics mode for this device.</span></span> <span data-ttu-id="f714f-114">L'HDC risultante può essere usato per eseguire qualsiasi operazione grafica sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f714f-114">The resulting hdc can be used to perform any graphics operation to the device.</span></span>

 

 



