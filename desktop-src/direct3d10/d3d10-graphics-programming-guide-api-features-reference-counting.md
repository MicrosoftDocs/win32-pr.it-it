---
description: Le funzioni set Direct3D 10 non contengono un riferimento a un oggetto dispositivo-figlio.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Conteggio dei riferimenti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80745c7af251294dca279a023f541b6485d2c3e01da22d2b8432e7220ac9bbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793261"
---
# <a name="reference-counting-direct3d-10"></a>Conteggio dei riferimenti (Direct3D 10)

Le funzioni set Direct3D 10 non contengono un riferimento a un oggetto dispositivo-figlio. Ciò significa che ogni applicazione deve contenere un riferimento a un oggetto dispositivo-figlio per tutto il tempo in cui l'oggetto deve essere associato alla pipeline. Quando il conteggio dei riferimenti di un oggetto scende a zero, l'oggetto verrà scollegato dalla pipeline ed eliminato. Questo stile di riferimento che contiene è noto anche come delimitazione dei riferimenti deboli perché ogni percorso di associazione della pipeline contiene un riferimento debole all'interfaccia o all'oggetto a esso associato.

Esempio:


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





Differenze tra Direct3D 9 e Direct3D 10:

- In Direct3D 9 le funzioni set contengono un riferimento agli oggetti dispositivo; nelle funzioni set Direct3D 10 non contengono un riferimento agli oggetti dispositivo-figlio.



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




