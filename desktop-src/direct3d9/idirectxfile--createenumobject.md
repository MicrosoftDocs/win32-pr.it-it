---
description: Crea un oggetto enumeratore. Deprecato.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: Metodo IDirectXFile::CreateEnumObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1af10a0f46877a159ab8c6543fba9c1406d083e6b3f4a57cf1c41b9fb2d92612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985151"
---
# <a name="idirectxfilecreateenumobject-method"></a>Metodo IDirectXFile::CreateEnumObject

Crea un oggetto enumeratore. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pvSource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore ai dati il cui contenuto dipende dal valore di dwLoadOptions

</dd> <dt>

*dwLoadOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DXFILELOADOPTIONS**](dxfile.md)**

Valore che specifica l'origine dei dati. Questo valore può essere uno dei flag DXFILELOAD \_ xxx nelle [costanti DXFILE](dxfile.md).

</dd> <dt>

*ppEnumObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***

Indirizzo di un puntatore a [**un'interfaccia IDirectXFileEnumObject,**](idirectxfileenumobject.md) che rappresenta l'oggetto enumeratore creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, \_ DXFILEERR BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questo metodo, usare uno dei metodi IDirectXFileEnumObject per recuperare un oggetto dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 
