---
description: Recupera l'ID modello in questo oggetto dati del file.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: Metodo ID3DXFileData::GetType (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e386c27638ced2be41197bf5f0095a481365dd19bc39b69d5d13d1ac8ec8dc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748531"
---
# <a name="id3dxfiledatagettype-method"></a>Metodo ID3DXFileData::GetType

Recupera l'ID modello in questo oggetto dati del file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pType* \[ Pollici\]
</dt> <dd>

Tipo: **[**CONST GUID**](guid.md) \***

Puntatore al GUID che rappresenta il modello in questo oggetto dati di file.

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

 

 




