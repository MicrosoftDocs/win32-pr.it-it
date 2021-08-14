---
description: Accede ai dati del file con estensione x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: Metodo ID3DXFileData::Lock (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c052f570b3206c5a0661a4cf4ab38b259fb476f4eda1322df80e709608d09bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520708"
---
# <a name="id3dxfiledatalock-method"></a>Metodo ID3DXFileData::Lock

Accede ai dati del file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Puntatore alla dimensione dei dati del file con estensione x.

</dd> <dt>

*ppData* \[ Pollici\]
</dt> <dd>

Tipo: **const \* \* VOID**

Indirizzo di un puntatore per ricevere il puntatore a interfaccia dell'oggetto dati del file [**ID3DXFileData.**](id3dxfiledata.md) Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Il *puntatore ppData* è valido solo durante un **ID3DXFileData::Lock** ... [**Sequenza ID3DXFileData::Unlock.**](id3dxfiledata--unlock.md) È possibile effettuare più chiamate di blocco. Tuttavia, è necessario assicurarsi che il numero di chiamate di blocco corrisponda al numero di chiamate di sblocco.

Poiché non è garantito che i dati dei file siano allineati correttamente con i limiti di byte, è necessario accedere a *ppData* con puntatori UNALIGNED.

Non è garantito che i valori dei parametri restituiti siano validi a causa di un possibile danneggiamento del file. Pertanto, il codice deve verificare i valori dei parametri restituiti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
