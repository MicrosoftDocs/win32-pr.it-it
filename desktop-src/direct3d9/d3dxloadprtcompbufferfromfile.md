---
description: Carica in memoria un buffer PRT (Precomputed Radiance Transfer) compresso salvato su disco.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: Funzione D3DXLoadPRTCompBufferFromFile (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a05a5712961e8bf72f4eb67f7e644d0f41150b812800fc1c0bd9bca464e3f54f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027381"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a>Funzione D3DXLoadPRTCompBufferFromFile

Carica in memoria un buffer PRT (Precomputed Radiance Transfer) compresso salvato su disco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome del file da cui caricare i dati compressi del buffer.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Indirizzo di un puntatore [**all'oggetto ID3DXPRTCompBuffer di**](id3dxprtcompbuffer.md) output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadPRTCompBufferFromFileW. In caso contrario, la chiamata di funzione viene risolta in D3DXLoadPRTCompBufferFromFileA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento di radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
