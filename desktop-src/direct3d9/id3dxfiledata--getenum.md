---
description: Recupera l'oggetto di enumerazione in questo oggetto dati del file.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: Metodo ID3DXFileData::GetEnum (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79ee6272f6b685c5e80b7c7b76b39925a08bb67cc07ba7af23a5b276b414f194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748551"
---
# <a name="id3dxfiledatagetenum-method"></a>Metodo ID3DXFileData::GetEnum

Recupera l'oggetto di enumerazione in questo oggetto dati del file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppObj* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Indirizzo di un puntatore per ricevere l'oggetto di enumerazione in questo oggetto dati file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




