---
description: 'Metodo ID3DXPRTBuffer::GetNumChannels: recupera il numero di canali di colore usati in memoria per archiviare i campioni.'
ms.assetid: dd1e3590-78e1-41a2-9f15-79389d9a210a
title: Metodo ID3DXPRTBuffer::GetNumChannels (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.GetNumChannels
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a86bac0a827839180cf746f762c39c583e64a4f80c4ebeac1d4e5e936ca69c51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294104"
---
# <a name="id3dxprtbuffergetnumchannels-method"></a>Metodo ID3DXPRTBuffer::GetNumChannels

Recupera il numero di canali di colore utilizzati in memoria per archiviare i campioni.

## <a name="syntax"></a>Sintassi


```C++
UINT GetNumChannels();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Restituisce il numero di canali di colore utilizzati in memoria per archiviare i campioni. Il valore sarà in genere 1 per rappresentare i valori di luminance o 3 per rappresentare i valori RGB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
