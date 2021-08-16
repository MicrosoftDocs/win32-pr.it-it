---
description: Definisce le opzioni per l'esecuzione di calcoli della distanza geodetica, quando si adatta una trama a una superficie curva. Usare questo flag per scegliere tra calcoli di alta qualità e calcoli rapidi durante il calcolo di un at atlas delle trame.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Enumerazione D3DXUVATLAS (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 1edcf2b1cbe2363f805bee1f5eb67f5558702ea9e163a865e1a6c51d6f5ed6ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523837"
---
# <a name="d3dxuvatlas-enumeration"></a>Enumerazione D3DXUVATLAS

Definisce le opzioni per l'esecuzione di calcoli della distanza geodetica, quando si adatta una trama a una superficie curva. Usare questo flag per scegliere tra calcoli di alta qualità e calcoli rapidi durante il calcolo di un at atlas delle trame.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**IMPOSTAZIONE PREDEFINITA D3DXUVATLAS \_**
</dt> <dd>

Alle mesh con più di 25.000 visi verrà applicato il metodo di distanza geodasica veloce, mentre alle mesh con meno di 25.000 visi verrà applicato il metodo di distanza geodetica di qualità superiore.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ GEODESIC \_ FAST**
</dt> <dd>

Usa approssimazioni per migliorare la velocità di creazione dei grafici a costo di aggiungere un'estensione o più grafici che vengono restituiti per la mesh.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**QUALITÀ GEODETICA D3DXUVATLAS \_ \_**
</dt> <dd>

Offre grafici di qualità migliore, ma richiede più tempo e memoria rispetto alla velocità.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




