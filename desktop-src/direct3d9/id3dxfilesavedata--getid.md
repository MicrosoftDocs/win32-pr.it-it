---
description: Recupera il GUID del nodo dati del file ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'Metodo ID3DXFileSaveData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323061"
---
# <a name="id3dxfilesavedatagetid-method"></a>Metodo ID3DXFileSaveData:: GetId

Recupera il GUID del nodo dati del file [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PID* \[ out\]
</dt> <dd>

Tipo: **LPGUID**

Puntatore a un GUID per ricevere l'ID del nodo dati del file. Se l'oggetto non dispone di un ID, il valore del parametro restituito sarà GUID \_ null.

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

 

 




