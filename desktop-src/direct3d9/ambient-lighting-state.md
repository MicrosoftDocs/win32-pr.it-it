---
description: La luce ambientale è la luce che si irradia da tutte le direzioni. Per informazioni sul modo in cui Direct3D usa la luce di ambiente, vedere matematica dell'illuminazione (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Stato illuminazione ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bd604941961f5b4abdb301d5c23efba9980791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127235"
---
# <a name="ambient-lighting-state-direct3d-9"></a>Stato illuminazione ambiente (Direct3D 9)

La luce ambientale è la luce che si irradia da tutte le direzioni. Per informazioni sul modo in cui Direct3D usa la luce di ambiente, vedere [matematica dell'illuminazione (Direct3D 9)](mathematics-of-lighting.md).

Un'applicazione C++ imposta il colore dell'illuminazione ambientale richiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e passando il valore enumerato D3DRS \_ ambiente come primo parametro. Il secondo parametro è un valore di colore. Il valore predefinito è zero.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
