---
description: Aggiunge un oggetto dati come figlio dell'oggetto ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'Metodo ID3DXFileSaveObject:: AddDataObject (D3DX9Xof. h)'
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
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322622"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a>Metodo ID3DXFileSaveObject:: AddDataObject

Aggiunge un oggetto dati come figlio dell'oggetto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

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

*rguidTemplate* \[ in\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID che rappresenta il modello dell'oggetto dati.

</dd> <dt>

*szName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'oggetto dati. Specificare **null** se l'oggetto non ha un nome.

</dd> <dt>

*PID* \[ in\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntatore a un GUID che rappresenta l'oggetto dati. Specificare **null** se l'oggetto non dispone di un GUID.

</dd> <dt>

*cbSize* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**

Dimensioni dell'oggetto dati, in byte.

</dd> <dt>

*pvData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore a un buffer contenente tutti i dati necessari nell'oggetto dati.

</dd> <dt>

*ppObj* \[ in, retval\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXFileSaveData**](id3dxfilesavedata.md) , che rappresenta il nodo dati del file a cui verrà aggiunto l'oggetto dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Se un oggetto riferimento ai dati fa riferimento all'oggetto dati, il szName o il parametro pId deve essere non **null**.

Salvare i dati creati su disco usando il metodo [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 
