---
description: Recupera l'ID modello in questo oggetto dati file.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'Metodo ID3DXFileData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401993"
---
# <a name="id3dxfiledatagettype-method"></a>Metodo ID3DXFileData:: GetType

Recupera l'ID modello in questo oggetto dati file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pType* \[ in\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntatore al GUID che rappresenta il modello in questo oggetto dati file.

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

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




