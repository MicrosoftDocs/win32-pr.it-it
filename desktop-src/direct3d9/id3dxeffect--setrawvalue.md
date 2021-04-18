---
description: Impostare un intervallo contiguo di costanti dello shader con una copia di memoria.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'Metodo ID3DXEffect:: SetRawValue (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322353"
---
# <a name="id3dxeffectsetrawvalue-method"></a>Metodo ID3DXEffect:: SetRawValue

Impostare un intervallo contiguo di costanti dello shader con una copia di memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle per il valore da impostare o il nome del valore passato come stringa. Il passaggio di un handle è più efficiente. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Tipo: **void \***

Puntatore a un buffer contenente i dati da impostare. SetRawValue verifica la presenza di memoria valida, ma non esegue alcuna verifica dei dati validi.

</dd> <dt>

*OffsetInBytes* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di byte compresi tra l'inizio dei dati degli effetti e l'inizio delle costanti degli effetti che si intende impostare.

</dd> <dt>

*Byte* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Dimensioni del buffer da impostare, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: E \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

SetRawValue è un modo molto rapido per impostare le costanti degli effetti poiché esegue una copia di memoria senza eseguire la convalida o la conversione dei dati, ad esempio la conversione di una matrice row-major in una matrice column-major. Usare SetRawValue per impostare una serie di costanti di effetto contigue. Ad esempio, è possibile impostare una matrice di venti matrici con 20 chiamate a [**ID3DXBaseEffect:: sematrix**](id3dxbaseeffect--setmatrix.md) o usando un singolo SetRawValue.

Si prevede che tutti i valori siano matrix4x4s o float4s e che tutte le matrici siano in ordine colonna-Major. Viene eseguito il cast dei valori int o float in un float4; è quindi consigliabile usare SetRawValue solo con i dati float4 o matrix4x4.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
