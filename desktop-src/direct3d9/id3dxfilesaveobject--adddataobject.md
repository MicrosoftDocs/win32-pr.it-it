---
description: Aggiunge un oggetto dati come figlio dell'oggetto ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: Metodo ID3DXFileSaveObject::AddDataObject (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8a1bdea820b90ae68c819ae2755f2abecd892cfd362116f6da37cb643a254048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802416"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a>Metodo ID3DXFileSaveObject::AddDataObject

Aggiunge un oggetto dati come figlio [**dell'oggetto ID3DXFileSaveData.**](id3dxfilesavedata.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
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

*pId* \[ Pollici\]
</dt> <dd>

Tipo: **[**CONST GUID**](guid.md) \***

Puntatore a un GUID che rappresenta l'oggetto dati. Specificare **NULL** se l'oggetto non dispone di un GUID.

</dd> <dt>

*cbSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Dimensioni dell'oggetto dati, in byte.

</dd> <dt>

*pvData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore a un buffer contenente tutti i dati necessari nell'oggetto dati.

</dd> <dt>

*ppObj* \[ in, retval\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXFileSaveData,**](id3dxfilesavedata.md) che rappresenta il nodo dati del file a cui verrà aggiunto l'oggetto dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Se un oggetto riferimento ai dati farà riferimento all'oggetto dati, il parametro szName o pId deve essere diverso da **NULL.**

Salvare i dati creati su disco usando il [**metodo ID3DXFileSaveObject::Save.**](id3dxfilesaveobject--save.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 
