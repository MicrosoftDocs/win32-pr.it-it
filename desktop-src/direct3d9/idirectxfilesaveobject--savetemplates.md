---
description: Salva i modelli in un file DirectX. Deprecato.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'Metodo IDirectXFileSaveObject:: SaveTemplates (DXFile. h)'
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
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354669"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>Metodo IDirectXFileSaveObject:: SaveTemplates

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

*cTemplates* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero totale di modelli da salvare.

</dd> <dt>

*ppguidTemplates* \[ in\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* \* const**

Indirizzo di un puntatore a una matrice di GUID per tutti i modelli da salvare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Il seguente frammento di codice fornisce una chiamata di esempio a **IDirectXFileSaveObject:: SaveTemplates** e il contenuto di esempio per la matrice a cui punta ppguidTemplates.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Dopo aver usato questo metodo per salvare i modelli, usare il metodo [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare un oggetto dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
