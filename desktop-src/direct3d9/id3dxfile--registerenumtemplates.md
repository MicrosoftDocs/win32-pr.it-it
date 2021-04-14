---
description: Registra i modelli personalizzati, dato un oggetto di enumerazione ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'Metodo ID3DXFile:: RegisterEnumTemplates (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401988"
---
# <a name="id3dxfileregisterenumtemplates-method"></a>Metodo ID3DXFile:: RegisterEnumTemplates

Registra i modelli personalizzati, dato un oggetto di enumerazione [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pEnum* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***

Puntatore a un oggetto di enumerazione [**ID3DXFileEnumObject**](id3dxfileenumobject.md) contenente i modelli.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK.

Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Quando questo metodo viene chiamato, copia i modelli archiviati con ID3DXFileEnumObject, che rappresenta il file, nell'archivio dei modelli locale dell'oggetto [**ID3DXFile**](id3dxfile.md) .

Se non è disponibile un puntatore [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , chiamare invece il metodo [**RegisterTemplates**](id3dxfile--registertemplates.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




