---
description: Introduzione alla grafica DirectX
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Introduzione alla grafica DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e0bc8a3485091ec8b8fa53c8245a3a4916e11af96493d4895585061f2b080f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830571"
---
# <a name="getting-started-with-directx-graphics"></a>Introduzione alla grafica DirectX

La grafica Microsoft DirectX offre un set di API che è possibile usare per creare giochi e altre applicazioni multimediali ad alte prestazioni. La grafica DirectX include il supporto per la grafica 2D e 3D ad alte prestazioni.

Per la grafica 3D, usare l'API Microsoft Direct3D 11. Anche se si dispone di hardware Microsoft Direct3D 9 o Microsoft Direct3D 10 livello, è possibile usare l'API Direct3D 11 e impostare come destinazione un dispositivo con livello di funzionalità [9](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) x o livello di funzionalità \_ 10 \_ x. Per informazioni su come sviluppare grafica 3D con DirectX, vedi Creare grafica [3D con DirectX.](/previous-versions/windows/apps/hh465137(v=win.10)
)

Per grafica e testo 2D, usare Direct2D e [DirectWrite](./directwrite/direct-write-portal.md) anziché Windows Graphics Device Interface (GDI).

Per comporre bitmap popolate da Direct3D 11 o Direct2D, [usare DirectComposition.](./directcomp/directcomposition-portal.md)

Per informazioni su come creare un'app Windows Store che usa DirectX, vedere Creare la [prima app Windows Store con DirectX.](/previous-versions/windows/apps/br229580(v=win.10)
) È possibile usare il [**Windows. Classe UI::Xaml::Controls::SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) per creare app DirectX ad alte prestazioni con una sovrimpressione dell'interfaccia utente XAML. Per altre informazioni sulla combinazione di XAML e DirectX in un'app Windows, vedi [Interoperabilità DirectX e XAML.](/previous-versions/windows/apps/hh825871(v=win.10))

Per informazioni su come creare un driver di visualizzazione per Windows 8, vedere Roadmap [for the Windows Display Driver Model (WDDM) (Guida](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo)di orientamento per il modello di Windows Display Driver Model (WDDM).

Se è necessaria la documentazione per le versioni precedenti di DirectX, vedere [Grafica DirectX classica.](/windows/desktop/classic-directx-graphics)


 

 
