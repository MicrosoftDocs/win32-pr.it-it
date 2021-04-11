---
description: Crea un oggetto binario e lo aggiunge come oggetto figlio. Deprecato.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'Metodo IDirectXFileData:: AddBinaryObject (DXFile. h)'
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
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234947"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a>Metodo IDirectXFileData:: AddBinaryObject

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

*szName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'oggetto. Specificare **null** se l'oggetto non necessita di un nome.

</dd> <dt>

*pguid* \[ in\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntatore al GUID che rappresenta l'oggetto. Specificare **null** se l'oggetto non necessita di un GUID.

</dd> <dt>

*szMimeType* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al tipo MIME dell'oggetto.

</dd> <dt>

*pvData* \[ in\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore ai dati dell'oggetto.

</dd> <dt>

*cbSize* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Dimensioni del buffer a cui punta pvData in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileBinary:: GetMimeType**](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
