---
title: Metodo ID3DX11EffectVariable AsMatrix (D3dx11effect.h)
description: Ottiene una variabile di matrice.
ms.assetid: 5d2baf65-ab0d-44df-bc6f-6ffae16cbb01
keywords:
- Metodo AsMatrix Direct3D 11
- Metodo AsMatrix Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , AsMatrix method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 294f3f6a01d88f92f606e5120edbfa8d5086f2e0173375fd78f5525c17c4f1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531502"
---
# <a name="id3dx11effectvariableasmatrix-method"></a>Metodo ID3DX11EffectVariable::AsMatrix

Ottiene una variabile di matrice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectMatrixVariable* AsMatrix();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***

Puntatore a una variabile di matrice. Vedere [**ID3DX11EffectMatrixVariable.**](id3dx11effectmatrixvariable.md)

## <a name="remarks"></a>Commenti

AsMatrix restituisce una versione della variabile dell'effetto specializzata in una variabile di matrice. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile dell'effetto non contiene dati di matrice.

Le applicazioni possono testare la validità dell'oggetto restituito chiamando [**IsValid.**](id3dx11effectvariable-isvalid.md)

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





