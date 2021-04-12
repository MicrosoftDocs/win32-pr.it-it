---
description: Le funzioni set di Direct3D 10 non contengono un riferimento a un oggetto dispositivo-figlio.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Conteggio dei riferimenti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6482918601f163bdea92291eb3927899ca797d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523226"
---
# <a name="reference-counting-direct3d-10"></a>Conteggio dei riferimenti (Direct3D 10)

Le funzioni set di Direct3D 10 non contengono un riferimento a un oggetto dispositivo-figlio. Ciò significa che ogni applicazione deve contenere un riferimento a un oggetto dispositivo-figlio per il periodo di tempo in cui l'oggetto deve essere associato alla pipeline. Quando il conteggio dei riferimenti di un oggetto scende a zero, l'oggetto non viene associato dalla pipeline e viene eliminato definitivamente. Questo stile di riferimento è noto anche come tenuta di riferimento debole, perché ogni percorso di associazione della pipeline contiene un riferimento debole all'interfaccia/oggetto associato.

Ad esempio:


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





|                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> In Direct3D 9, le funzioni set contengono un riferimento agli oggetti dispositivo. nelle funzioni set di Direct3D 10 non è presente un riferimento agli oggetti Device-Child.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




