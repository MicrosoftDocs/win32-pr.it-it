---
title: Come aggiungere il supporto per più monitor
description: DirectWrite include il supporto per sistemi con più monitor.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bbfb2c803372e52128cd62dddeec407985e4180039d84f9aed66092149911b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048891"
---
# <a name="how-to-add-support-for-multiple-monitors"></a>Come aggiungere il supporto per più monitor

[DirectWrite](direct-write-portal.md) include il supporto per sistemi con più monitor. Monitor diversi possono avere geometria in pixel diversa (RGB, BGR o FLAT) o altri attributi. Per altre informazioni sulla geometria pixel, vedere l'argomento [**di riferimento DWRITE \_ PIXEL \_ GEOMETRY.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) Questo argomento illustra come aggiungere il supporto per più monitor all'DirectWrite applidato.

Per supportare più monitor, è necessario gestire il messaggio **della \_ finestra WM WINDOWPOSCHANGED.** Questo messaggio viene inviato quando la finestra viene spostata, pertanto è necessario controllare se la finestra è stata spostata in un monitor diverso, come illustrato nel codice seguente.


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



Se la finestra si trova in un nuovo monitoraggio, è necessario creare parametri di rendering per il nuovo monitoraggio usando il [**metodo IDWriteFactory::CreateMonitorRenderingParams.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams)

> [!Note]  
> Non usare il [**metodo IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) per creare i parametri di rendering, perché crea sempre i parametri per il monitoraggio primario.

 

Quando si ha un oggetto [**IDWriteRenderingParams,**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) impostare i parametri di rendering per la destinazione di rendering usando il metodo [**ID2DRenderTarget::SetTextRenderingParams.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams)

Usare infine la funzione [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) per fare in modo che la finestra venga ridisegnata con i nuovi parametri di rendering.

 

 