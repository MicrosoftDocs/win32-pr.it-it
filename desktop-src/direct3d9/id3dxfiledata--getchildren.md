---
description: Recupera il numero di elementi figlio in questo oggetto dati di file.
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: Metodo ID3DXFileData::GetChildren (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dca2197a321efea6cf86ee0f38b1778935e5f4cb336b55b5d662e49a4465162a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493841"
---
# <a name="id3dxfiledatagetchildren-method"></a>Metodo ID3DXFileData::GetChildren

Recupera il numero di elementi figlio in questo oggetto dati di file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*puiChildren* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Indirizzo di un puntatore per ricevere il numero di elementi figlio in questo oggetto dati file.

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

 

 
