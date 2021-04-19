---
description: Un effetto viene creato caricando il valore nel Framework degli effetti.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Creazione di un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304602"
---
# <a name="create-an-effect-direct3d-10"></a>Creazione di un effetto (Direct3D 10)

Un effetto viene creato caricando il valore nel Framework degli effetti. Se l'effetto non è mai stato compilato, verrà compilato al momento della creazione. Gli effetti già caricati nella memoria possono essere creati chiamando [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md). Nell'esempio di codice seguente viene usato [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) per creare un effetto da un file.


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



Per la lettura di un effetto sono necessari gli stessi parametri della compilazione di un effetto, oltre a un dispositivo e a un pool.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



