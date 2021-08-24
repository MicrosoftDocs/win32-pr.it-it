---
description: Recupera il GUID di questo nodo dati del file ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: Metodo ID3DXFileSaveData::GetId (D3DX9Xof.h)
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
ms.openlocfilehash: 4e6f502357510cc1c8fc51e9ada844a988a79b1571435639586380929b121c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748501"
---
# <a name="id3dxfilesavedatagetid-method"></a>Metodo ID3DXFileSaveData::GetId

Recupera il GUID di questo nodo dati del file [**ID3DXFileSaveData.**](id3dxfilesavedata.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pId* \[ Cambio\]
</dt> <dd>

Tipo: **LPGUID**

Puntatore a un GUID per ricevere l'ID di questo nodo dati file. Se l'oggetto non ha ID, il valore del parametro restituito sarà GUID \_ NULL.

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

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




