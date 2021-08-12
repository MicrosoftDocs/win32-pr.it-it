---
title: Funzione D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un processore di dati da usare con un thread pump. | Funzione D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex.h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- Funzione D3DX11CreateAsyncTextureInfoProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da992c258fe79bd1ed81274495e884339f40aed337fcf11665ec27110afaf422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536260"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a>Funzione D3DX11CreateAsyncTextureInfoProcessor

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.

 

Creare un processore di dati da usare con un [**thread pump**](id3dx11threadpump.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pImageInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)) quando viene creato il processore di dati. Impostare questo valore su **NULL** per leggere le caratteristiche di una trama quando la trama viene caricata.

</dd> <dt>

*ppDataProcessor* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questa API crea un'interfaccia del processore di dati. [**D3DX11CreateAsyncTextureProcessor crea**](d3dx11createasynctextureprocessor.md) l'interfaccia del processore di dati e carica la trama.

Non esiste alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.

Per Windows app di Store, gli esempi DirectX (ad esempio, l'esempio di esercitazione [Direct3D)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Per le app desktop Win32, è possibile usare il runtime di concorrenza [per](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) implementare qualcosa di simile al modello di programmazione asincrona Windows Runtime.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

