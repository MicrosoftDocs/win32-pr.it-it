---
title: Metodo GetBool ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Ottenere una variabile booleana.
ms.assetid: 9d2789af-c59f-4d2d-87c6-9f36286e8a15
keywords:
- Metodo GetBool Direct3D 11
- Metodo GetBool Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- Interfaccia ID3DX11EffectScalarVariable Direct3D 11, Metodo GetBool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 754dd8856876ca441e83267250dcfad4f4011c69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762322"
---
# <a name="id3dx11effectscalarvariablegetbool-method"></a>Metodo ID3DX11EffectScalarVariable:: GetBool

Ottenere una variabile booleana.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBool(
   BOOL *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pValue* 
</dt> <dd>

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***

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

 

