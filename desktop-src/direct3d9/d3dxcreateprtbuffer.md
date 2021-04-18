---
description: Crea un buffer PRT (pre-Computed Radiance Transfer) che può essere compresso o riempito da un simulatore. Questa funzione deve essere usata per creare buffer per vertice o volume.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: Funzione D3DXCreatePRTBuffer (D3DX9Mesh. h)
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
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322734"
---
# <a name="d3dxcreateprtbuffer-function"></a>D3DXCreatePRTBuffer (funzione)

Crea un buffer PRT (pre-Computed Radiance Transfer) che può essere compresso o riempito da un simulatore. Questa funzione deve essere usata per creare buffer per vertice o volume.

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

*NumSamples valore* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di vertici (o Texel) campionati.

</dd> <dt>

*NumCoeffs* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di coefficienti per percorso di esempio. Quando si usa il PRT sferica (SH), il numero di coefficienti deve essere Order ², dove Order è l'ordine della valutazione SH. L'ordine deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. Il livello della valutazione è Order-1.

</dd> <dt>

*NumChannels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di canali dei colori da impostare nella rete. Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.

</dd> <dt>

*ppBuffer* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Indirizzo di un puntatore all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Quando viene creato il buffer, tutti i valori vengono inizializzati su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento Radiance pre-calcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
