---
description: Crea un oggetto enumeratore in grado di leggere un file con estensione x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'Metodo ID3DXFile:: CreateEnumObject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323074"
---
# <a name="id3dxfilecreateenumobject-method"></a>Metodo ID3DXFile:: CreateEnumObject

Crea un oggetto enumeratore in grado di leggere un file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pvSource* \[ out\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Origine dati. Una delle due versioni seguenti:

-   Un nome file
-   Struttura [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)
-   Struttura [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)

A seconda del valore di loadflags.

</dd> <dt>

*loadflags* \[ in\]
</dt> <dd>

Tipo: **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**

Valore che specifica l'origine dei dati. Questo valore può essere uno dei flag [ \_ FILELOADOPTIONS di D3DXF](d3dxf.md) .

</dd> <dt>

*ppEnumObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , che rappresenta l'oggetto enumeratore creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questo metodo, utilizzare uno dei metodi [**ID3DXFileEnumObject**](id3dxfileenumobject.md) per recuperare un oggetto dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
