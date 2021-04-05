---
description: Recupera l'oggetto ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'Metodo ID3DXFileEnumObject:: GetFile (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969410"
---
# <a name="id3dxfileenumobjectgetfile-method"></a>Metodo ID3DXFileEnumObject:: GetFile

Recupera l'oggetto [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFile* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXFile**](id3dxfile.md) , che rappresenta l'oggetto restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 




