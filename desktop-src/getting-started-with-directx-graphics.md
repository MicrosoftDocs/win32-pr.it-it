---
description: .
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Introduzione alla grafica DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5278e759ea0faf04ac8b247ad3ea1c687dd205c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050102"
---
# <a name="getting-started-with-directx-graphics"></a>Introduzione alla grafica DirectX

Microsoft DirectX Graphics fornisce un set di API che è possibile usare per creare giochi e altre applicazioni multimediali ad alte prestazioni. La grafica DirectX include il supporto per la grafica 2D e 3D ad alte prestazioni.

Per le immagini 3D, usare l'API Microsoft Direct3D 11. Anche se si dispone di hardware Microsoft Direct3D 9 o Microsoft Direct3D a livello 10, è possibile usare l'API Direct3D 11 e definire come destinazione un dispositivo a livello di [funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 x o a livello di \_ funzionalità 10 \_ x. Per informazioni su come sviluppare grafica 3D con DirectX, vedere [creare grafica 3D con DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

Per la grafica e il testo 2D, utilizzare Direct2D e [DirectWrite](./directwrite/direct-write-portal.md) anziché Windows Graphics Device Interface (GDI).

Per comporre bitmap che vengono popolate da Direct3D 11 o Direct2D, usare [DirectComposition](./directcomp/directcomposition-portal.md).

Per informazioni su come creare un'app di Windows Store che usa DirectX, vedere [creare la prima app di Windows Store con DirectX](/previous-versions/windows/apps/br229580(v=win.10)
). È possibile usare la classe [**Windows. UI:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) per creare app DirectX a prestazioni elevate con una sovrapposizione dell'interfaccia utente XAML. Per altre informazioni sulla combinazione di XAML e DirectX in un'app di Windows, vedere [interoperabilità con DirectX e XAML](/previous-versions/windows/apps/hh825871(v=win.10)).

Per informazioni sulla creazione di un driver di visualizzazione per Windows 8, vedere [Roadmap for the Windows Display Driver Model (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Se è necessaria la documentazione per le versioni precedenti di DirectX, vedere la pagina relativa alla [grafica DirectX classica](/windows/desktop/classic-directx-graphics).


 

 
