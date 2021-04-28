---
description: 'Funzione D3DXGetImageInfoFromFile: recupera informazioni su un determinato file di immagine.'
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: Funzione D3DXGetImageInfoFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb03b6482d140a3b78e43d8b99c60499ae6c8b16
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114495"
---
# <a name="d3dxgetimageinfofromfile-function"></a>Funzione D3DXGetImageInfoFromFile

Recupera informazioni su un determinato file di immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome file dell'immagine su cui recuperare le informazioni. Se sono definiti \_ unicode o UNICODE, questo tipo di parametro è LPCWSTR. In caso contrario, il tipo è LPCSTR.

</dd> <dt>

*pSrcInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntatore a [**una struttura D3DXIMAGE \_ INFO**](d3dximage-info.md) da riempire con la descrizione dei dati nel file di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

Questa funzione supporta sia stringhe Unicode che ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
