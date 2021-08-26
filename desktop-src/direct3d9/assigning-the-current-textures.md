---
description: Direct3D gestisce un elenco di un massimo di otto trame correnti. Unisce queste trame a tutte le primitive di cui esegue il rendering. Solo le trame create come puntatori all'interfaccia di trama possono essere usate nel set di trame correnti.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Assegnazione delle trame correnti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b2a9ac0b61f7a7d0a9b3ee27c7a9b7e6b8cd4d48fda33959462e26ad6958ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069421"
---
# <a name="assigning-the-current-textures-direct3d-9"></a>Assegnazione delle trame correnti (Direct3D 9)

Direct3D gestisce un elenco di un massimo di otto trame correnti. Unisce queste trame a tutte le primitive di cui esegue il rendering. Solo le trame create come puntatori all'interfaccia di trama possono essere usate nel set di trame correnti.

Le applicazioni chiamano [**il metodo IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per assegnare trame nel set di trame correnti. Il primo parametro deve essere un numero compreso tra 0 e 7 inclusi. Passare il puntatore dell'interfaccia della trama come secondo parametro.

L'esempio di codice C++ seguente illustra come assegnare una trama al set di trame correnti.


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> I dispositivi software non supportano l'assegnazione di una trama a più fasi di trama alla volta.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione delle trame](texture-blending.md)
</dt> </dl>

 

 
