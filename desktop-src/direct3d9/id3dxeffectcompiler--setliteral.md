---
description: Consente di abilitare o disabilitare lo stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'Metodo ID3DXEffectCompiler:: seliteral (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354354"
---
# <a name="id3dxeffectcompilersetliteral-method"></a>Metodo ID3DXEffectCompiler:: seliteral

Consente di abilitare o disabilitare lo stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco per un parametro. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*Valore letterale* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Impostare su **true** per fare in modo che il parametro sia un valore letterale e **false** se il parametro può modificare il valore durante la durata dello shader.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo cambia solo se il parametro è un valore letterale o meno. Per modificare il valore di un parametro, usare un metodo come [**ID3DXBaseEffect::**](id3dxbaseeffect--setbool.md) SetValue o [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).

Questa funzione deve essere chiamata prima che l'effetto venga compilato. Di seguito è riportato un esempio di come è possibile usare questa funzione:


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Utilizzi e valori letterali (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler:: GetLiteral**](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
