---
description: Crea un'istanza di un oggetto DirectXFile. Deprecato.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Funzione DirectXFileCreate (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 6dbcf4836c33fd2acfc1adc21e47430a54ba7c54aeb2b220199846d31572619e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952181"
---
# <a name="directxfilecreate-function"></a>Funzione DirectXFileCreate

Crea un'istanza di un oggetto DirectXFile. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Tipo: **[ **LPDIRECTXFILE**](idirectxfile.md)\***

Indirizzo di un puntatore a [**un'interfaccia IDirectXFile,**](idirectxfile.md) che rappresenta l'oggetto DirectXFile creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questa funzione, usare [**RegisterTemplates**](idirectxfile--registertemplates.md) per registrare i modelli, [**CreateEnumObject**](idirectxfile--createenumobject.md) per creare un oggetto enumeratore o [**CreateSaveObject**](idirectxfile--createsaveobject.md) per creare un oggetto save.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dxof.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni file X](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](idirectxfile--createsaveobject.md)
</dt> <dt>

[**RegisterTemplates**](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




