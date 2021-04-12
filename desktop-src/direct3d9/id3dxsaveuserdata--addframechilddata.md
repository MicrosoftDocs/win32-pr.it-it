---
description: Aggiungere i dati figlio al frame.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'Metodo ID3DXSaveUserData:: AddFrameChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235190"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a>Metodo ID3DXSaveUserData:: AddFrameChildData

Aggiungere i dati figlio al frame.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFrame* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Puntatore a un contenitore mesh. Vedere [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofSave* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntatore a un oggetto di salvataggio file con estensione x. Usare il puntatore per chiamare [**ID3DXFileSaveObject:: AddDataObject**](id3dxfilesaveobject--adddataobject.md) per aggiungere un oggetto dati figlio. Non salvare i dati con [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofFrameData* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Puntatore a un nodo dati del file con estensione x. Usare il puntatore per chiamare [**ID3DXFileSaveData:: AddDataObject**](id3dxfilesavedata--adddataobject.md) per aggiungere un oggetto dati figlio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni. In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.

## <a name="remarks"></a>Commenti

[**ID3DXSaveUserData:: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) e [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) forniscono un meccanismo per l'aggiunta di un modello a un file con estensione x per il salvataggio dei dati utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
