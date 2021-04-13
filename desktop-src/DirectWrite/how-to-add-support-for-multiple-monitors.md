---
title: Come aggiungere il supporto per più monitoraggi
description: DirectWrite include il supporto per i sistemi con più monitor.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c5d95d0e727b4184a2dcce1720379231ce22a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399310"
---
# <a name="how-to-add-support-for-multiple-monitors"></a><span data-ttu-id="a05ad-103">Come aggiungere il supporto per più monitoraggi</span><span class="sxs-lookup"><span data-stu-id="a05ad-103">How to Add Support for Multiple Monitors</span></span>

<span data-ttu-id="a05ad-104">[DirectWrite](direct-write-portal.md) include il supporto per i sistemi con più monitor.</span><span class="sxs-lookup"><span data-stu-id="a05ad-104">[DirectWrite](direct-write-portal.md) includes support for systems with multiple monitors.</span></span> <span data-ttu-id="a05ad-105">Diversi monitoraggi possono avere una geometria di pixel diversa (RGB, BGR o FLAT) o altri attributi.</span><span class="sxs-lookup"><span data-stu-id="a05ad-105">Different monitors may have different pixel geometry (RGB, BGR, or FLAT) or other attributes.</span></span> <span data-ttu-id="a05ad-106">Per ulteriori informazioni sulla geometria dei pixel, vedere l'argomento di riferimento sulla [**\_ \_ geometria dei pixel DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) .</span><span class="sxs-lookup"><span data-stu-id="a05ad-106">For more information about pixel geometry, see the [**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) reference topic.</span></span> <span data-ttu-id="a05ad-107">In questo argomento viene illustrato come aggiungere il supporto per più monitoraggi all'applicazione DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="a05ad-107">This topic will show you how to add support for multiple monitors to your DirectWrite application.</span></span>

<span data-ttu-id="a05ad-108">Per supportare più monitoraggi, è necessario gestire il messaggio della **finestra \_ WINDOWPOSCHANGED WM** .</span><span class="sxs-lookup"><span data-stu-id="a05ad-108">In order to support multiple monitors, you must handle the **WM\_WINDOWPOSCHANGED** window message.</span></span> <span data-ttu-id="a05ad-109">Questo messaggio viene inviato quando la finestra viene spostata, quindi è necessario verificare se la finestra è stata spostata in un altro monitoraggio, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="a05ad-109">This message is sent when the window is moved, so you must check if the window has moved to a different monitor as shown in the following code.</span></span>


```C++
case WM_WINDOWPOSCHANGED:
    {
        HMONITOR monitor = MonitorFromWindow(hwnd, MONITOR_DEFAULTTONULL);
        if (monitor != g_monitor)
        {
            g_monitor = monitor;
            if (g_spRenderTarget != NULL)
            {
                IDWriteRenderingParams* pRenderingParams = NULL;
                g_spDWriteFactory->CreateMonitorRenderingParams(monitor, &pRenderingParams);

                g_spRenderTarget->SetTextRenderingParams(pRenderingParams);

                SafeRelease(&pRenderingParams);
            }

            InvalidateRect(hwnd, NULL, TRUE);
        }
    }
    break;
```



<span data-ttu-id="a05ad-110">Se la finestra si trova in un nuovo monitor, è necessario creare parametri di rendering per il nuovo monitoraggio usando il metodo [**IDWriteFactory archiviata nei:: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="a05ad-110">If the window is located on a new monitor, then you must create rendering parameters for the new monitor by using the [**IDWriteFactory::CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) method.</span></span>

> [!Note]  
> <span data-ttu-id="a05ad-111">Non usare il metodo [**IDWriteFactory archiviata nei:: CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) per creare i parametri di rendering, perché crea sempre parametri per il monitoraggio primario.</span><span class="sxs-lookup"><span data-stu-id="a05ad-111">Do not use the [**IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) method to create the rendering parameters, because it always creates parameters for the primary monitor.</span></span>

 

<span data-ttu-id="a05ad-112">Quando si dispone di un oggetto [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) , impostare i parametri di rendering per la destinazione di rendering usando il metodo [**ID2DRenderTarget:: SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="a05ad-112">When you have an [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) object, set the rendering parameters for the render target by using the [**ID2DRenderTarget::SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) method.</span></span>

<span data-ttu-id="a05ad-113">Infine, utilizzare la funzione [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) per fare in modo che la finestra venga ridisegnato con i nuovi parametri di rendering.</span><span class="sxs-lookup"><span data-stu-id="a05ad-113">Finally, use the [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) function to cause the window to redraw with the new rendering parameters.</span></span>

 

 