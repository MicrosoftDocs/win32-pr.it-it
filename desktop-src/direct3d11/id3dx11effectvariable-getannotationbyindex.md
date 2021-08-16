---
title: Metodo ID3DX11EffectVariable GetAnnotationByIndex (D3dx11effect.h)
description: Ottiene un'annotazione in base all'indice. | Metodo ID3DX11EffectVariable GetAnnotationByIndex (D3dx11effect.h)
ms.assetid: fc130098-0269-4c78-bc45-284aa0b77865
keywords:
- Metodo GetAnnotationByIndex Direct3D 11
- Metodo GetAnnotationByIndex Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , Metodo GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4319038fefa6539bf40834bfc1f00f4ea4a0cfb8b12c1c6719c884e413b3ae07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531145"
---
# <a name="id3dx11effectvariablegetannotationbyindex-method"></a>Metodo ID3DX11EffectVariable::GetAnnotationByIndex

Ottiene un'annotazione in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a [**id3DX11EffectVariable.**](id3dx11effectvariable.md)

## <a name="remarks"></a>Commenti

Gli annonazioni possono essere collegati a una tecnica, a un passaggio o a una variabile globale.

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

 

