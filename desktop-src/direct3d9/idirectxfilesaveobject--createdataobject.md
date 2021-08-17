---
description: Crea un oggetto dati. Deprecato.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: Metodo IDirectXFileSaveObject::CreateDataObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e1497ad06919833e0ba716877dc81b8df51a99361a49e43fa9a0f756e296040c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728913"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a>Metodo IDirectXFileSaveObject::CreateDataObject

Crea un oggetto dati. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rguidTemplate* \[ Pollici\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID che rappresenta il modello dell'oggetto dati.

</dd> <dt>

*szName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'oggetto dati. Specificare **NULL** se l'oggetto non ha un nome.

</dd> <dt>

*pguid* \[ Pollici\]
</dt> <dd>

Tipo: **[**CONST GUID**](guid.md) \***

Puntatore a un GUID che rappresenta l'oggetto dati. Specificare **NULL** se l'oggetto non dispone di un GUID.

</dd> <dt>

*cbSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Dimensioni dell'oggetto dati, in byte.

</dd> <dt>

*pvData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a un buffer contenente tutti i dati necessari del membro.

</dd> <dt>

*ppDataObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Indirizzo di un puntatore a [**un'interfaccia IDirectXFileData**](idirectxfiledata.md) che rappresenta l'oggetto dati del file creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Commenti

Se un oggetto riferimento ai dati farà riferimento all'oggetto dati, il parametro szName o pguid deve essere diverso da **NULL.**

Salvare i modelli usando il [**metodo IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) prima di salvare i dati creati da questo metodo. Salvare i dati creati usando il [**metodo IDirectXFileSaveObject::SaveData.**](idirectxfilesaveobject--savedata.md)

Se è necessario salvare dati facoltativi, usare il metodo [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) dopo aver utilizzato questo metodo e prima di [**usare IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md). Se l'oggetto ha oggetti figlio, aggiungerli prima di chiamare **IDirectXFileSaveObject::SaveData**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
