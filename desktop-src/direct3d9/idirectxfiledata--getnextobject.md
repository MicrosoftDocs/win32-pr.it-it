---
description: Recupera il successivo oggetto dati figlio, oggetto riferimento ai dati o oggetto binario nel file DirectX. Deprecato.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'Metodo IDirectXFileData:: GetNextObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323231"
---
# <a name="idirectxfiledatagetnextobject-method"></a>Metodo IDirectXFileData:: GetNextObject

Recupera il successivo oggetto dati figlio, oggetto riferimento ai dati o oggetto binario nel file DirectX. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppChildObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***

Indirizzo di un puntatore a un'interfaccia [**IDirectXFileObject**](idirectxfileobject.md) , che rappresenta l'interfaccia dell'oggetto del file dell'oggetto figlio restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS.

## <a name="remarks"></a>Commenti

Per determinare il tipo di oggetto recuperato, utilizzare QueryInterface per eseguire una query sull'oggetto recuperato per supportare le interfacce [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md)o [**IDirectXFileBinary**](idirectxfilebinary.md) . L'interfaccia supportata indica il tipo di oggetto (dati, riferimento ai dati o binario).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirectXFileBinary**](idirectxfilebinary.md)
</dt> <dt>

[**IDirectXFileData**](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileDataReference**](idirectxfiledatareference.md)
</dt> </dl>

 

 




