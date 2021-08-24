---
description: Questa funzione, che crea un oggetto shader-reflection per il recupero di informazioni su uno shader compilato, non esiste più. Usare invece D3DReflect o D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: Funzione D3DX10ReflectShader (D3DX10Core.h)
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
ms.openlocfilehash: 7694aa0dcfcc256358993f29c9ed448c1648b35768e5844a959726a6737c2371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753081"
---
# <a name="d3dx10reflectshader-function"></a>Funzione D3DX10ReflectShader

Questa funzione, che crea un oggetto shader-reflection per il recupero di informazioni su uno shader compilato, non esiste più. Usare invece [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) o [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).

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

*pShaderBytecode* \[ Pollici\]
</dt> <dd>

Tipo: **const \* void**

Puntatore allo shader compilato. Per ottenere questo puntatore, vedere [Recupero di un puntatore a uno shader compilato.](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)

</dd> <dt>

*BytecodeLength* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Lunghezza di pShaderBytecode.

</dd> <dt>

*ppReflector* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Indirizzo di un'interfaccia di reflection shader (vedere [**l'interfaccia ID3D10ShaderReflection1).**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 10 seguenti.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di creazione di un oggetto shader-reflection. L'esempio presuppone che si inizi con uno shader compilato (illustrato come


```
pVSBuf
```



che è possibile vedere in [HLSLWithoutFX10 Sample ( Esempio di HLSLWithoutFX10).](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)


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
| Intestazione<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
