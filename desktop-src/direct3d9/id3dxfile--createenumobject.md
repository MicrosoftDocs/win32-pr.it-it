---
description: Crea un oggetto enumeratore che leggerà un file con estensione x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: Metodo ID3DXFile::CreateEnumObject (D3DX9Xof.h)
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
ms.openlocfilehash: 528ab441da6cd4370de4ecad5d8490e6e74b5977672d0c7d4126cea1b7bab8fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044399"
---
# <a name="id3dxfilecreateenumobject-method"></a>Metodo ID3DXFile::CreateEnumObject

Crea un oggetto enumeratore che leggerà un file con estensione x.

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

*pvSource* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Origine dati. Una delle due versioni seguenti:

-   Nome di un file
-   Struttura [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)
-   Struttura [**\_ FILELOADRESOURCE D3DXF**](d3dxf-fileloadresource.md)

A seconda del valore di loadflags.

</dd> <dt>

*loadflags* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**

Valore che specifica l'origine dei dati. Questo valore può essere uno dei flag [D3DXF \_ FILELOADOPTIONS.](d3dxf.md)

</dd> <dt>

*ppEnumObj* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXFileEnumObject,**](id3dxfileenumobject.md) che rappresenta l'oggetto enumeratore creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questo metodo, usare uno dei metodi [**ID3DXFileEnumObject**](id3dxfileenumobject.md) per recuperare un oggetto dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
