---
description: Aggiunge un riferimento ai dati come figlio del nodo dati del file ID3DXFileSaveData. Il riferimento ai dati punta a un oggetto dati di file.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'Metodo ID3DXFileSaveData:: AddDataReference (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969408"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>Metodo ID3DXFileSaveData:: AddDataReference

Aggiunge un riferimento ai dati come figlio del nodo dati del file [**ID3DXFileSaveData**](id3dxfilesavedata.md) . Il riferimento ai dati punta a un oggetto dati di file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'oggetto dati da aggiungere per riferimento. Specificare **null** se l'oggetto dati non ha un nome.

</dd> <dt>

*PID* \[ in\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntatore a un GUID che rappresenta l'oggetto dati da aggiungere per riferimento. Se **null**, verrà aggiunto un riferimento che punta all'oggetto dati con il nome specificato da szName.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

L'oggetto dati di file a cui si fa riferimento deve avere un nome o un GUID. L'oggetto dati del file deve anche derivare da un altro oggetto padre [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
