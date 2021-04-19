---
description: Aggiungere un oggetto di primo livello prima della gerarchia dei frame.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'Metodo ID3DXSaveUserData:: AddTopLevelDataObjectsPre (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0194c8c9c6806f96cbe75394e6650ca3e7dc74b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323522"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a>Metodo ID3DXSaveUserData:: AddTopLevelDataObjectsPre

Aggiungere un oggetto di primo livello prima della gerarchia dei frame.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pXofSave* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Puntatore a un oggetto di salvataggio file con estensione x. Utilizzare questo puntatore per chiamare [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare l'oggetto dati da salvare. Quindi, chiamare [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) per salvare i dati.

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

 

 
