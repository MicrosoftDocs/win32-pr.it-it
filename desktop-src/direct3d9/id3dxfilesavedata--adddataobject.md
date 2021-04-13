---
description: Aggiunge un oggetto dati come figlio del nodo dati del file ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'Metodo ID3DXFileSaveData:: AddDataObject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355219"
---
# <a name="id3dxfilesavedataadddataobject-method"></a>Metodo ID3DXFileSaveData:: AddDataObject

Aggiunge un oggetto dati come figlio del nodo dati del file [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

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

Puntatore al nome dell'oggetto dati da aggiungere. Specificare **null** se l'oggetto non ha un nome.

</dd> <dt>

*PID* \[ in\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntatore a un GUID che rappresenta l'oggetto dati. L'oggetto dati deve essere stato registrato con [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) o [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md). Specificare **null** se l'oggetto non dispone di un GUID.

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

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
