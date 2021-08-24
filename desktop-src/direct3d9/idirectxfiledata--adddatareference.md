---
description: Crea e aggiunge un oggetto riferimento ai dati come oggetto figlio. Deprecato.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: Metodo IDirectXFileData::AddDataReference (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 4c291e4f5754975f7e564c8c579b3651b29f0e6b684ad474f2f8436875dbf078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747261"
---
# <a name="idirectxfiledataadddatareference-method"></a>Metodo IDirectXFileData::AddDataReference

Crea e aggiunge un oggetto riferimento ai dati come oggetto figlio. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szRef* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'oggetto dati di riferimento. Questo parametro può essere **NULL** se pguidRef fornisce un riferimento al GUID.

</dd> <dt>

*pguidRef* \[ Pollici\]
</dt> <dd>

Tipo: **[**CONST GUID**](guid.md) \***

Puntatore al GUID che rappresenta i dati. Questo parametro può essere **NULL** se szRef fornisce un riferimento al nome.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Commenti

Perché questo metodo riesca, il parametro szRef o pguidRef deve essere diverso da **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 
