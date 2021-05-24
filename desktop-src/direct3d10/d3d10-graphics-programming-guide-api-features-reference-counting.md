---
description: Le funzioni set Direct3D 10 non contengono un riferimento a un oggetto dispositivo-figlio.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Conteggio dei riferimenti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335455"
---
# <a name="reference-counting-direct3d-10"></a>Conteggio dei riferimenti (Direct3D 10)

Le funzioni set Direct3D 10 non contengono un riferimento a un oggetto dispositivo-figlio. Ciò significa che ogni applicazione deve contenere un riferimento a un oggetto dispositivo-figlio per tutto il tempo in cui l'oggetto deve essere associato alla pipeline. Quando il conteggio dei riferimenti di un oggetto scende a zero, l'oggetto verrà scollegato dalla pipeline ed eliminato. Questo stile di riferimento che contiene è noto anche come delimitazione dei riferimenti deboli perché ogni percorso di associazione della pipeline contiene un riferimento debole all'interfaccia o all'oggetto associato.

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





Differenze tra Direct3D 9 e Direct3D 10:

- In Direct3D 9 le funzioni set contengono un riferimento agli oggetti dispositivo; nelle funzioni set Direct3D 10 non contengono un riferimento agli oggetti dispositivo-figlio.



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




