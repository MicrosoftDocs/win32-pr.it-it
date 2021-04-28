---
description: 'Metodo ID3DXFileData::GetChild: recupera un oggetto figlio in questo oggetto dati file.'
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: Metodo ID3DXFileData::GetChild (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7fe6c0393e5cfb9ed8aeaf5808d33175e7f9bfe5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090379"
---
# <a name="id3dxfiledatagetchild-method"></a>Metodo ID3DXFileData::GetChild

Recupera un oggetto figlio in questo oggetto dati file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uiChild* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

ID dell'oggetto figlio da recuperare.

</dd> <dt>

*ppChild* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Indirizzo di un puntatore a ricevere il puntatore a interfaccia dell'oggetto figlio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
