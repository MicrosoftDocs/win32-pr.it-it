---
description: Direct3D mantiene un elenco di un massimo di otto trame correnti. Combina queste trame su tutte le primitive di cui esegue il rendering. Nel set di trame correnti è possibile usare solo trame create come puntatori dell'interfaccia di trama.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Assegnazione delle trame correnti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483981"
---
# <a name="assigning-the-current-textures-direct3d-9"></a>Assegnazione delle trame correnti (Direct3D 9)

Direct3D mantiene un elenco di un massimo di otto trame correnti. Combina queste trame su tutte le primitive di cui esegue il rendering. Nel set di trame correnti è possibile usare solo trame create come puntatori dell'interfaccia di trama.

Le applicazioni chiamano il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per assegnare trame al set di trame correnti. Il primo parametro deve essere un numero compreso nell'intervallo 0-7, inclusivo. Passare il puntatore all'interfaccia di trama come secondo parametro.

Nell'esempio di codice C++ riportato di seguito viene illustrato il modo in cui una trama può essere assegnata al set di trame correnti.


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> I dispositivi software non supportano l'assegnazione di una trama a più di una fase di trama alla volta.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di trame](texture-blending.md)
</dt> </dl>

 

 
