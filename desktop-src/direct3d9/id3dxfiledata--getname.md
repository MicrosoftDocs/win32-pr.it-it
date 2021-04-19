---
description: Recupera il nome di questo oggetto dati file.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'Metodo ID3DXFileData:: GetName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323070"
---
# <a name="id3dxfiledatagetname-method"></a>Metodo ID3DXFileData:: GetName

Recupera il nome di questo oggetto dati file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szName* \[ in\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Indirizzo di un puntatore per la ricezione del nome di questo oggetto dati file. Se questo parametro è **null**, puiSize restituirà la dimensione della stringa. Se szName punta alla memoria valida, il nome di questo oggetto dati file verrà copiato in szName fino al numero di caratteri specificato da puiSize.

</dd> <dt>

*puiSize* \[ in uscita\]
</dt> <dd>

Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)\***

Puntatore alla dimensione della stringa che rappresenta il nome di questo oggetto dati file. Questo parametro può essere **null** se szName fornisce un riferimento al nome. Questo parametro restituirà la dimensione della stringa se szName è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Affinché questo metodo abbia esito positivo, szName o *puiSize* deve essere non **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
