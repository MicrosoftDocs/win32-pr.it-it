---
description: Questa funzione, che crea un oggetto di Reflection shader per il recupero di informazioni su uno shader compilato, non esiste più. Usare invece D3DReflect o D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: Funzione D3DX10ReflectShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322771"
---
# <a name="d3dx10reflectshader-function"></a>D3DX10ReflectShader (funzione)

Questa funzione, che crea un oggetto di Reflection shader per il recupero di informazioni su uno shader compilato, non esiste più. Usare invece [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) o [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pShaderBytecode* \[ in\]
</dt> <dd>

Tipo: **const \* void**

Puntatore allo shader compilato. Per ottenere questo puntatore, vedere [ottenere un puntatore a uno shader compilato](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

</dd> <dt>

*BytecodeLength* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**

Lunghezza di pShaderBytecode.

</dd> <dt>

*ppReflector* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Indirizzo di un'interfaccia di Reflection shader (vedere [**interfaccia ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di creazione di un oggetto di Reflection shader. Nell'esempio si presuppone che si inizi con uno shader compilato (visualizzato come


```
pVSBuf
```



come è possibile vedere nell' [esempio HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
