---
title: Metodo ID3DX11EffectVectorVariable SetIntVectorArray (D3dx11effect.h)
description: Impostare una matrice di vettori a quattro componenti che contengono dati integer.
ms.assetid: c9e522d7-5545-4b91-b6b3-6fad9a151cb0
keywords:
- Metodo SetIntVectorArray Direct3D 11
- Metodo SetIntVectorArray Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- ID3DX11EffectVectorVariable interface Direct3D 11 , SetIntVectorArray method
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5260fd85461b23d02d9aa33619fcf2c00a81fcb63212d612e6e8920728bbefd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894541"
---
# <a name="id3dx11effectvectorvariablesetintvectorarray-method"></a>Metodo ID3DX11EffectVectorVariable::SetIntVectorArray

Impostare una matrice di vettori a quattro componenti che contengono dati integer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIntVectorArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Puntatore all'inizio dei dati da impostare.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Deve essere impostato su 0. è riservato per un uso futuro.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi della matrice da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

