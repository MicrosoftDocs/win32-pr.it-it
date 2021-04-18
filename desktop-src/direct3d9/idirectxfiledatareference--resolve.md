---
description: Risolve i riferimenti ai dati. Deprecato.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'Metodo IDirectXFileDataReference:: Resolve (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323228"
---
# <a name="idirectxfiledatareferenceresolve-method"></a>Metodo IDirectXFileDataReference:: Resolve

Risolve i riferimenti ai dati. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDataObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Indirizzo di un puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) , che rappresenta l'oggetto dati di file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileDataReference](idirectxfiledatareference.md)
</dt> </dl>

 

 




