---
description: Carica in memoria un buffer PRT (pre-Computed Radiance Transfer) salvato su disco.
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: Funzione D3DXLoadPRTBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10caedc9b77ef97f4d070ce82392b5da1de54fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354224"
---
# <a name="d3dxloadprtbufferfromfile-function"></a>D3DXLoadPRTBufferFromFile (funzione)

Carica in memoria un buffer PRT (pre-Computed Radiance Transfer) salvato su disco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome del file da cui caricare i dati del buffer.

</dd> <dt>

*ppBuffer* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Indirizzo di un puntatore all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadPRTBufferFromFileW. In caso contrario, la chiamata di funzione viene risolta in D3DXLoadPRTBufferFromFileA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento Radiance pre-calcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
