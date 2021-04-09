---
description: Per impostazione predefinita, quando si esegue il test di profondità su una superficie di rendering, il sistema Direct3D aggiorna la superficie di destinazione di rendering se il valore di profondità corrispondente (z o w) per ogni punto è minore del valore nel buffer di profondità.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Modifica delle funzioni di confronto del buffer di profondità (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749063"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a>Modifica delle funzioni di confronto del buffer di profondità (D3D9)

Per impostazione predefinita, quando si esegue il test di profondità su una superficie di rendering, il sistema Direct3D aggiorna la superficie di destinazione di rendering se il valore di profondità corrispondente (z o w) per ogni punto è minore del valore nel buffer di profondità. In un'applicazione C++ è possibile modificare il modo in cui il sistema esegue i confronti sui valori di profondità chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) con il parametro *state* impostato su D3DRS \_ ZFUNC. Il parametro *value* deve essere impostato su un valore nel tipo enumerato [**D3DCMPFUNC**](./d3dcmpfunc.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer di profondità](depth-buffers.md)
</dt> </dl>

 

 
