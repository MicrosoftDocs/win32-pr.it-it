---
description: Crea e aggiunge un oggetto riferimento ai dati come oggetto figlio. Deprecato.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'Metodo IDirectXFileData:: AddDataReference (DXFile. h)'
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
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322539"
---
# <a name="idirectxfiledataadddatareference-method"></a>Metodo IDirectXFileData:: AddDataReference

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

*szRef* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'oggetto dati a cui si fa riferimento. Questo parametro può essere **null** se pguidRef fornisce un riferimento al GUID.

</dd> <dt>

*pguidRef* \[ in\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntatore al GUID che rappresenta i dati. Questo parametro può essere **null** se szRef fornisce un riferimento al nome.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Commenti

Affinché questo metodo abbia esito positivo, il parametro szRef o pguidRef deve essere non **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 
