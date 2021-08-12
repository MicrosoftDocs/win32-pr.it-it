---
description: Crea un buffer PRT (Precomputed Radiance Transfer) che può essere compresso o riempito da un simulatore. Questa funzione deve essere usata per creare buffer per vertice o volume.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: Funzione D3DXCreatePRTBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff7293fd866bed8ef5bea46fd783b27672c4c53ee61786f75146ea45efd8a509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299276"
---
# <a name="d3dxcreateprtbuffer-function"></a>Funzione D3DXCreatePRTBuffer

Crea un buffer PRT (Precomputed Radiance Transfer) che può essere compresso o riempito da un simulatore. Questa funzione deve essere usata per creare buffer per vertice o volume.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumSamples* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici (o texel) campionati.

</dd> <dt>

*NumCoeff* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di coefficienti per ogni posizione del campione. Quando si usa sferica armonica (SH) PRT, il numero di coefficienti deve essere Order², dove Order è l'ordine della valutazione SH. L'ordine deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi. Il grado di valutazione è Order - 1.

</dd> <dt>

*NumChannels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di canali di colore da impostare nella mesh. Impostare su 1 per specificare materiali grigi (R = G = B) o 3 per abilitare gli effetti di colorazione.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Indirizzo di un puntatore [**all'oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Quando viene creato il buffer, tutti i valori vengono inizializzati su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento della radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
