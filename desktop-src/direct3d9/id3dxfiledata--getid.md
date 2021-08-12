---
description: Recupera il GUID di questo oggetto dati file.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: Metodo ID3DXFileData::GetId (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a9a1cbf98792b0ac36c35aabf40b8c125a497201b27c6a161c0706f077ffc491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295327"
---
# <a name="id3dxfiledatagetid-method"></a>Metodo ID3DXFileData::GetId

Recupera il GUID di questo oggetto dati file.

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

Puntatore a un GUID per ricevere l'ID di questo oggetto dati file. Se l'oggetto dati del file non ha ID, il valore del parametro restituito sarà GUID \_ NULL.

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

 

 




