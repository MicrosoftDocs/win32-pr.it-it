---
title: Metodo ID3DX11EffectScalarVariable SetValue (D3dx11effect. h)
description: Impostare una variabile booleana.
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- Metodo sebool Direct3D 11
- Metodo sebool Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- Interfaccia ID3DX11EffectScalarVariable Direct3D 11, metodo sebool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1d3670b3a41f47bf1b5ec7ac3d2fb93441e72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982412"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a>Metodo ID3DX11EffectScalarVariable:: SetValue

Impostare una variabile booleana.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Valore* 
</dt> <dd>

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Puntatore alla variabile.

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

