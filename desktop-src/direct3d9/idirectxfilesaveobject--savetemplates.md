---
description: Salva i modelli in un file DirectX. Deprecato.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: Metodo IDirectXFileSaveObject::SaveTemplates (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 87ec95932b26877354c22089a97b249bd542aa841552c3e3f9e4827a20f6d608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292222"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>Metodo IDirectXFileSaveObject::SaveTemplates

Salva i modelli in un file DirectX. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cTemplates* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero totale di modelli da salvare.

</dd> <dt>

*ppguidTemplates* \[ Pollici\]
</dt> <dd>

Tipo: **[**CONST GUID**](guid.md) \* \***

Indirizzo di un puntatore a una matrice di GUID per tutti i modelli da salvare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Il frammento di codice seguente fornisce una chiamata di esempio a **IDirectXFileSaveObject::SaveTemplates** e il contenuto di esempio per la matrice a cui punta ppguidTemplates.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Dopo aver utilizzato questo metodo per salvare i modelli, usare il metodo [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare un oggetto dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
