---
description: Direct3D fornisce le funzioni seguenti per determinare il supporto hardware.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Determinazione del supporto hardware (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42dda0aa1e1d5d75d2c8b6f0364c08daa836e7d2f0996252748bbb49b3d2a4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730634"
---
# <a name="determining-hardware-support-direct3d-9"></a>Determinazione del supporto hardware (Direct3D 9)

Direct3D fornisce le funzioni seguenti per determinare il supporto hardware.

-   [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    Usato per verificare se un formato di superficie può essere usato come trama, se un formato di superficie può essere usato come trama e destinazione di rendering o se un formato di superficie può essere usato come buffer depth-stencil. Inoltre, questo metodo viene usato per verificare il supporto del formato buffer depth e il supporto del formato buffer depth-stencil.

-   [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    Usato per verificare la capacità di un dispositivo di eseguire l'accelerazione hardware, la capacità di un dispositivo di creare una catena di scambio per la presentazione o la capacità di un dispositivo di eseguire il rendering nel formato di visualizzazione corrente.

-   [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    Utilizzato per verificare se un formato buffer depth-stencil è compatibile con un formato di destinazione di rendering. Si noti che prima di chiamare questo metodo, l'applicazione deve chiamare [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) nei formati depth-stencil e render-target.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
