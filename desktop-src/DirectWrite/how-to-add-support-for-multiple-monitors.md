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
# <a name="how-to-add-support-for-multiple-monitors"></a>Come aggiungere il supporto per più monitoraggi

[DirectWrite](direct-write-portal.md) include il supporto per i sistemi con più monitor. Diversi monitoraggi possono avere una geometria di pixel diversa (RGB, BGR o FLAT) o altri attributi. Per ulteriori informazioni sulla geometria dei pixel, vedere l'argomento di riferimento sulla [**\_ \_ geometria dei pixel DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . In questo argomento viene illustrato come aggiungere il supporto per più monitoraggi all'applicazione DirectWrite.

Per supportare più monitoraggi, è necessario gestire il messaggio della **finestra \_ WINDOWPOSCHANGED WM** . Questo messaggio viene inviato quando la finestra viene spostata, quindi è necessario verificare se la finestra è stata spostata in un altro monitoraggio, come illustrato nel codice seguente.


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



Se la finestra si trova in un nuovo monitor, è necessario creare parametri di rendering per il nuovo monitoraggio usando il metodo [**IDWriteFactory archiviata nei:: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .

> [!Note]  
> Non usare il metodo [**IDWriteFactory archiviata nei:: CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) per creare i parametri di rendering, perché crea sempre parametri per il monitoraggio primario.

 

Quando si dispone di un oggetto [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) , impostare i parametri di rendering per la destinazione di rendering usando il metodo [**ID2DRenderTarget:: SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .

Infine, utilizzare la funzione [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) per fare in modo che la finestra venga ridisegnato con i nuovi parametri di rendering.

 

 