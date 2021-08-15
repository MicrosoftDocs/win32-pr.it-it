---
description: Aggiungere un oggetto di primo livello prima della gerarchia dei frame.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: Metodo ID3DXSaveUserData::AddTopLevelDataObjectsPre (D3dx9anim.h)
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
ms.openlocfilehash: 52052a24c34c99260a68cd5cdeaa7487e6b71c086ac30922a06de241de8319ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801163"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a>Metodo ID3DXSaveUserData::AddTopLevelDataObjectsPre

Aggiungere un oggetto di primo livello prima della gerarchia dei frame.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddTopLevelDataObjectsPre(
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

 

 
