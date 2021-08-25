---
description: Aggiungere dati figlio alla mesh.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: Metodo ID3DXSaveUserData::AddMeshChildData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397dc9ade32222dd98e050110811464f6544a1d0af52729417c61fbc3367bdbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893311"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a>Metodo ID3DXSaveUserData::AddMeshChildData

Aggiungere dati figlio alla mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMeshContainer* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***

Puntatore a un contenitore mesh. Vedere [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> <dt>

*pXofSave* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntatore a un oggetto di salvataggio di file con estensione x. Usare il puntatore per chiamare [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) per aggiungere un oggetto dati figlio. Non salvare i dati con [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofMeshData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Puntatore a un nodo dati di file con estensione x. Usare il puntatore per chiamare [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) per aggiungere un oggetto dati figlio.

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

 

 
