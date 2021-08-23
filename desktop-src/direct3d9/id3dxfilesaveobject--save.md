---
description: Salva un oggetto dati e i relativi elementi figlio in un file con estensione x su disco.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: Metodo ID3DXFileSaveObject::Save (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a49c4776f9ce590d287869436b329ddf9a378e73f04f0127246fc890944ffee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563961"
---
# <a name="id3dxfilesaveobjectsave-method"></a>Metodo ID3DXFileSaveObject::Save

Salva un oggetto dati e i relativi elementi figlio in un file con estensione x su disco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere il seguente: D3DXFERR \_ BADOBJECT.

## <a name="remarks"></a>Commenti

Al termine di questo metodo, [**ID3DXFileSaveObject::AddDataObject,**](id3dxfilesaveobject--adddataobject.md) [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) e [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) non possono più essere chiamati fino a quando non viene creato un nuovo [**oggetto ID3DXFile.**](id3dxfile.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




