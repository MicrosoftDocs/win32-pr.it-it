---
description: Direct3D fornisce le funzioni seguenti per determinare il supporto hardware.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Determinazione del supporto hardware (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303926"
---
# <a name="determining-hardware-support-direct3d-9"></a>Determinazione del supporto hardware (Direct3D 9)

Direct3D fornisce le funzioni seguenti per determinare il supporto hardware.

-   [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    Usato per verificare se un formato di superficie può essere usato come trama, se un formato di superficie può essere usato come trama e una destinazione di rendering o se un formato di superficie può essere usato come buffer di stencil di profondità. Questo metodo viene inoltre usato per verificare il supporto del formato del buffer di profondità e il supporto del formato di buffer dello stencil Depth.

-   [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    Usato per verificare la capacità di un dispositivo di eseguire l'accelerazione hardware, la capacità di un dispositivo di creare una catena di scambio per la presentazione o la possibilità di eseguire il rendering del dispositivo nel formato di visualizzazione corrente.

-   [**IDirect3D9:: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    Utilizzato per verificare se un formato di buffer di stencil Depth è compatibile con un formato di destinazione di rendering. Si noti che prima di chiamare questo metodo, l'applicazione deve chiamare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) sia nei formati depth-stencil che di rendering-target.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
