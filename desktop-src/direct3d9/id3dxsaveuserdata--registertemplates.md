---
description: Callback che consente all'utente di registrare un modello di file con estensione x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: Metodo ID3DXSaveUserData::RegisterTemplates (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a41a43f8f319ee09f24c4f62092e4718773dc312cb7886b0fc7c95781e614c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628731"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>Metodo ID3DXSaveUserData::RegisterTemplates

Callback che consente all'utente di registrare un modello di file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pXFileApi* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXFILE**](id3dxfile.md)**

Usare questo puntatore per registrare i modelli di file con estensione x definiti dall'utente. Vedere [**ID3DXFile**](id3dxfile.md). Non utilizzare questo parametro per aggiungere oggetti dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti di questo metodo vengono implementati da un programmatore di applicazioni. In generale, se non si verifica alcun errore, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo in modo che restituisca un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR,**](./d3dxerr.md)in quanto anche [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) avrà esito negativo e restituirà l'errore.

## <a name="remarks"></a>Commenti

**ID3DXSaveUserData::RegisterTemplates** e [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) forniscono un meccanismo per aggiungere un modello a un file con estensione x per salvare i dati utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
