---
description: Ottiene l'interfaccia ID3DXFile dell'oggetto che ha creato questo oggetto ID3DXFileSaveObject.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'Metodo ID3DXFileSaveObject:: GetFile (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401986"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a>Metodo ID3DXFileSaveObject:: GetFile

Ottiene l'interfaccia [**ID3DXFile**](id3dxfile.md) dell'oggetto che ha creato questo oggetto [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFile* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DXFile**](id3dxfile.md)**

Indirizzo di un puntatore a un oggetto [**ID3DXFile**](id3dxfile.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, e \_ nointerface, e \_ pointer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




