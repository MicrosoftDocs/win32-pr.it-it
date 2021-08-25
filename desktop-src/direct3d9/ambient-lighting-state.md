---
description: La luce ambientale è la luce circostante che emana da tutte le direzioni. Per informazioni su come Direct3D usa la luce ambientale, vedere Matematica dell'illuminazione (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Stato di illuminazione ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc32a6ec654bd30627c853bc00c90e94b6008e769fb3aa708e963a9430e0dc85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952691"
---
# <a name="ambient-lighting-state-direct3d-9"></a>Stato di illuminazione ambiente (Direct3D 9)

La luce ambientale è la luce circostante che emana da tutte le direzioni. Per informazioni sul modo in cui Direct3D usa la luce ambientale, vedere [Matematica dell'illuminazione (Direct3D 9).](mathematics-of-lighting.md)

Un'applicazione C++ imposta il colore dell'illuminazione ambiente richiamando il metodo [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e passando il valore enumerato D3DRS AMBIENT come primo \_ parametro. Il secondo parametro è un valore di colore. Il valore predefinito è zero.


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

 

 
