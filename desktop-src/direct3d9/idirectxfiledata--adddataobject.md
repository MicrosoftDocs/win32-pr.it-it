---
description: Aggiunge un oggetto dati come oggetto figlio. Deprecato.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: Metodo IDirectXFileData::AddDataObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: db11f5f3c0d9078663c87db8948bc483ab05d229cd4d7fd0950efaf5143e1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491831"
---
# <a name="idirectxfiledataadddataobject-method"></a>Metodo IDirectXFileData::AddDataObject

Aggiunge un oggetto dati come oggetto figlio. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataObj* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

Puntatore a [**un'interfaccia IDirectXFileData,**](idirectxfiledata.md) che rappresenta l'oggetto dati file da aggiungere come oggetto figlio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Commenti

Usare il [**metodo IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare l'oggetto [**IDirectXFileData**](idirectxfiledata.md) prima di chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




