---
description: Caricare i dati di primo livello da un file con estensione x.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'Metodo ID3DXLoadUserData:: LoadTopLevelData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323472"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a>Metodo ID3DXLoadUserData:: LoadTopLevelData

Caricare i dati di primo livello da un file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pXofChildData* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Puntatore a una struttura di dati del file con estensione x. Questa operazione è definita in dxfile. h.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni. In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da D3DERR o D3DXERR, in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




