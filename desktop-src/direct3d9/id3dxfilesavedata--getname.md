---
description: Recupera il nome di questo nodo dati del file ID3DXFileSaveData.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: Metodo ID3DXFileSaveData::GetName (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7aa6ef69a5296830b2f3bb992fb24ac23fa58adeeea629fd0e1bdeacf6173344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856650"
---
# <a name="id3dxfilesavedatagetname-method"></a>Metodo ID3DXFileSaveData::GetName

Recupera il nome di questo nodo dati del file [**ID3DXFileSaveData.**](id3dxfilesavedata.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Indirizzo di un puntatore per ricevere il nome di questo nodo dati file. Se questo parametro è **NULL,** *puiSize* restituirà le dimensioni della stringa. Se szName punta a una memoria valida, il nome di questo nodo dati file verrà copiato in szName fino al numero di caratteri specificato da *puiSize* .

</dd> <dt>

*puiSize* \[ in, out\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Puntatore alla dimensione della stringa che rappresenta il nome di questo nodo dati file. Questo parametro può essere **NULL** se szName fornisce un riferimento al nome. Questo parametro restituirà le dimensioni della stringa se szName è **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Per l'esito positivo di questo metodo, *szName* o *puiSize* deve essere diverso da **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
