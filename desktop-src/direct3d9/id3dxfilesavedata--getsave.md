---
description: Recupera un puntatore a questo nodo dati del file ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'Metodo ID3DXFileSaveData:: getsave (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235195"
---
# <a name="id3dxfilesavedatagetsave-method"></a>Metodo ID3DXFileSaveData:: getsave

Recupera un puntatore a questo nodo dati del file [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) che rappresenta questo nodo dati del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




