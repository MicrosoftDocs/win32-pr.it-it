---
description: Crea un oggetto binario e lo aggiunge come oggetto figlio. Deprecato.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: Metodo IDirectXFileData::AddBinaryObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d619fde6cd5d22f161188d46f710caeadfaedba2fbcf1167486e05dee539fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728977"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a>Metodo IDirectXFileData::AddBinaryObject

Crea un oggetto binario e lo aggiunge come oggetto figlio. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'oggetto. Specificare **NULL** se l'oggetto non richiede un nome.

</dd> <dt>

*pguid* \[ Pollici\]
</dt> <dd>

Tipo: **[**CONST GUID**](guid.md) \***

Puntatore al GUID che rappresenta l'oggetto . Specificare **NULL** se l'oggetto non richiede un GUID.

</dd> <dt>

*szMimeType* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al tipo MIME dell'oggetto.

</dd> <dt>

*pvData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore ai dati dell'oggetto.

</dd> <dt>

*cbSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Dimensioni del buffer a cui punta pvData, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileBinary::GetMimeType**](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
