---
description: Aggiungere un oggetto di primo livello dopo la gerarchia dei frame.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: Metodo ID3DXSaveUserData::AddTopLevelDataObjectsPost (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPost
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd0d631a814b25e8ff99272a29af377941e2a6865bd41e6a2fb2c6bcc8fc59a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727821"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a>Metodo ID3DXSaveUserData::AddTopLevelDataObjectsPost

Aggiungere un oggetto di primo livello dopo la gerarchia dei frame.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pXofSave* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntatore a un oggetto di salvataggio di file con estensione x. Usare questo puntatore per chiamare [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare l'oggetto dati da salvare. Chiamare quindi [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) per salvare i dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti di questo metodo vengono implementati da un programmatore di applicazioni. In generale, se non si verifica alcun errore, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo in modo che restituisca un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR,**](./d3dxerr.md)perché in questo modo anche [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) avrà esito negativo e restituirà l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
