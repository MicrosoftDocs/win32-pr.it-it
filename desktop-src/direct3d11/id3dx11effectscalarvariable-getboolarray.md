---
title: Metodo GetBoolArray ID3DX11EffectScalarVariable (D3dx11effect.h)
description: Ottiene una matrice di variabili booleane.
ms.assetid: 0335417a-a0aa-4157-881d-7828ffb3f47a
keywords:
- Metodo GetBoolArray Direct3D 11
- Metodo GetBoolArray Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- INTERFACCIA ID3DX11EffectScalarVariable Direct3D 11, metodo GetBoolArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBoolArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ad7cb09788d8eabc75917e371b7cde33b5cd64abc24c4309182e925281d823
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952731"
---
# <a name="id3dx11effectscalarvariablegetboolarray-method"></a>Metodo ID3DX11EffectScalarVariable::GetBoolArray

Ottiene una matrice di variabili booleane.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBoolArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)\***

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

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

