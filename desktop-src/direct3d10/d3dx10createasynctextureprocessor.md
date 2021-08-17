---
description: 'Funzione D3DX10CreateAsyncTextureProcessor: creare un processore di dati da usare con un thread pump.'
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Funzione D3DX10CreateAsyncTextureProcessor (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d245a96181e194479b0c5e115b3b3aea89096da8176713047578a93264e470da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852361"
---
# <a name="d3dx10createasynctextureprocessor-function"></a>Funzione D3DX10CreateAsyncTextureProcessor

Creare un processore di dati da usare con un [**thread pump.**](id3dx10threadpump.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore all'interfaccia deviva (vedere [**ID3D10Device Interface).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> <dt>

*pLoadInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) quando viene creato il processore di dati. Impostare questa proprietà su **NULL** per leggere le caratteristiche di una trama quando la trama viene caricata.

</dd> <dt>

*ppDataProcessor* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**l'interfaccia ID3DX10DataProcessor).**](id3dx10dataprocessor.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questa API crea un'interfaccia del processore di dati e carica la trama. [**D3DX10CreateAsyncTextureInfoProcessor crea**](d3dx10createasynctextureinfoprocessor.md) l'interfaccia del processore di dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




