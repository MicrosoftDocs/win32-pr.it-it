---
description: Nota Invece di usare questa funzione legacy, è consigliabile usare l'API D3DDisassemble. Questa funzione, che disassembla uno shader compilato in una stringa di testo che contiene istruzioni di assembly e assegnazioni di registro, non esiste più.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: Funzione D3DX10DisassembleShader (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: bd69b6dc2cede96e6ca07983195d202cfd248633f44a13fe1967393c446ca329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753221"
---
# <a name="d3dx10disassembleshader-function"></a>Funzione D3DX10DisassembleShader

> [!Note]  
> Anziché usare questa funzione legacy, è consigliabile usare l'API [**D3DDisassemble.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble)

 

Questa funzione, che disassembla uno shader compilato in una stringa di testo che contiene istruzioni di assembly e assegnazioni di registro, non esiste più. Usare invece [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pShader* \[ Pollici\]
</dt> <dd>

Tipo: **const \* void**

Puntatore allo [**shader compilato.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)

</dd> <dt>

*BytecodeLength* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Dimensioni di pShader.

</dd> <dt>

*EnableColorCode* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Includere tag HTML nell'output per colorare il risultato.

</dd> <dt>

*pComments* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa di commento nella parte superiore dello shader che identifica le costanti e le variabili dello shader.

</dd> <dt>

*ppDisassembly* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un buffer (vedere [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene lo shader disassemblato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 10 seguenti.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questo testo restituito include un'intestazione con la versione del compilatore HLSL usata per generare questo oggetto, i commenti che descrivono il layout di memoria dei buffer costanti usati dallo shader, le firme di input e output e i punti di associazione delle risorse.

Di seguito è riportato un esempio di disassembling di uno shader compilato. L'esempio presuppone che si inizi con uno shader compilato (illustrato come *pVSBuf,* che è possibile vedere in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
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

 

 
