---
description: Aggiungere i dati figlio alla rete.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'Metodo ID3DXSaveUserData:: AddMeshChildData (D3dx9anim. h)'
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
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235189"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a>Metodo ID3DXSaveUserData:: AddMeshChildData

Aggiungere i dati figlio alla rete.

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

*pMeshContainer* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***

Puntatore a un contenitore mesh. Vedere [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> <dt>

*pXofSave* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntatore a un oggetto di salvataggio file con estensione x. Usare il puntatore per chiamare [**ID3DXFileSaveObject:: AddDataObject**](id3dxfilesaveobject--adddataobject.md) per aggiungere un oggetto dati figlio. Non salvare i dati con [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofMeshData* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Puntatore a un nodo dati del file con estensione x. Usare il puntatore per chiamare [**ID3DXFileSaveData:: AddDataObject**](id3dxfilesavedata--adddataobject.md) per aggiungere un oggetto dati figlio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni. In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
