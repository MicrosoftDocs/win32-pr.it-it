---
description: Callback che consente all'utente di registrare un modello di file con estensione x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'Metodo ID3DXSaveUserData:: RegisterTemplates (D3dx9anim. h)'
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
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323521"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>Metodo ID3DXSaveUserData:: RegisterTemplates

Callback che consente all'utente di registrare un modello di file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pXFileApi* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXFILE**](id3dxfile.md)**

Utilizzare questo puntatore per registrare i modelli di file con estensione x definiti dall'utente. Vedere [**ID3DXFile**](id3dxfile.md). Non utilizzare questo parametro per aggiungere oggetti dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni. In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.

## <a name="remarks"></a>Commenti

**ID3DXSaveUserData:: RegisterTemplates** e [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) forniscono un meccanismo per l'aggiunta di un modello a un file con estensione x per il salvataggio dei dati utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
