---
description: Aggiunge un riferimento ai dati come figlio di questo nodo dati del file ID3DXFileSaveData. Il riferimento ai dati punta a un oggetto dati file.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: Metodo ID3DXFileSaveData::AddDataReference (D3DX9Xof.h)
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
ms.openlocfilehash: 862df88701cffd1059ca67e086cd49d05174bc66e9fa13807df2d2aeb0c9ff1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121350"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>Metodo ID3DXFileSaveData::AddDataReference

Aggiunge un riferimento ai dati come figlio di questo nodo dati del file [**ID3DXFileSaveData.**](id3dxfilesavedata.md) Il riferimento ai dati punta a un oggetto dati file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'oggetto dati da aggiungere per riferimento. Specificare **NULL** se l'oggetto dati non ha un nome.

</dd> <dt>

*pId* \[ Pollici\]
</dt> <dd>

Tipo: **[**CONST GUID**](guid.md) \***

Puntatore a un GUID che rappresenta l'oggetto dati da aggiungere per riferimento. Se **NULL,** verrà aggiunto un riferimento che punta all'oggetto dati con il nome specificato da szName.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'oggetto dati di file a cui si fa riferimento deve avere un nome o un GUID. L'oggetto dati del file deve derivare anche da un oggetto [**ID3DXFileSaveData**](id3dxfilesavedata.md) padre diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
