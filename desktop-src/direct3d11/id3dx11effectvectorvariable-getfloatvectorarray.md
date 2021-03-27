---
title: Metodo ID3DX11EffectVectorVariable GetFloatVectorArray (D3dx11effect. h)
description: Ottenere una matrice di vettori a quattro componenti che contengono dati a virgola mobile.
ms.assetid: 30ecbd97-c16d-4ea9-b7d9-364887f42a04
keywords:
- Metodo GetFloatVectorArray Direct3D 11
- Metodo GetFloatVectorArray Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11, metodo GetFloatVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a4c53b884c623ca3d11fb4a9a44660ce21d8a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982400"
---
# <a name="id3dx11effectvectorvariablegetfloatvectorarray-method"></a>Metodo ID3DX11EffectVectorVariable:: GetFloatVectorArray

Ottenere una matrice di vettori a quattro componenti che contengono dati a virgola mobile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Puntatore all'inizio dei dati da impostare.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Deve essere impostato su 0; Questa operazione è riservata per un utilizzo futuro.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi di matrice da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

