---
description: Caricare i dati figlio mesh da un file con estensione x.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: Metodo ID3DXLoadUserData::LoadMeshChildData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd4aaa857ac89594b1114612c59f959f0d91b050f6f9c0f0c9290798acf829f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120825"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a>Metodo ID3DXLoadUserData::LoadMeshChildData

Caricare i dati figlio mesh da un file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMeshContainer* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Puntatore a un contenitore mesh. Vedere [**D3DXMESHCONTAINER.**](d3dxmeshcontainer.md)

</dd> <dt>

*pXofChildData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Puntatore a una struttura di dati di file con estensione x. Questo valore è definito in Dxfile.h.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti di questo metodo vengono implementati da un programmatore di applicazioni. In generale, se non si verifica alcun errore, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo in modo che restituisca un messaggio di errore appropriato da D3DERR o D3DXERR, perché anche [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) avrà esito negativo e restituirà l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




