---
description: Salva un oggetto dati e i relativi elementi figlio in un file DirectX. Deprecato.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: Metodo IDirectXFileSaveObject::SaveData (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 293525d570540e00da4e8ac7680cf850b253c7e3ccbe3ffd152b639d0bc139cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747271"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a>Metodo IDirectXFileSaveObject::SaveData

Salva un oggetto dati e i relativi elementi figlio in un file DirectX. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataObj* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

Puntatore a [**un'interfaccia IDirectXFileData,**](idirectxfiledata.md) che rappresenta l'oggetto dati del file da salvare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> </dl>

 

 




