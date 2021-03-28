---
title: Funzione D3DX11CreateAsyncTextureProcessor (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un elaboratore di dati da utilizzare con una pompa di thread. | Funzione D3DX11CreateAsyncTextureProcessor (D3DX11tex. h)
ms.assetid: 4f23d265-b326-4449-b7ca-dd0596511b35
keywords:
- Funzione D3DX11CreateAsyncTextureProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612be6da4dce05ccae368edc4effea83a823dcff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996017"
---
# <a name="d3dx11createasynctextureprocessor-function"></a>D3DX11CreateAsyncTextureProcessor (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.

 

Creare un elaboratore di dati da utilizzare con una [**pompa di thread**](id3dx11threadpump.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateAsyncTextureProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntatore a Devive (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).

</dd> <dt>

*pLoadInfo* \[ in\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX11DataProcessor**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Questa API crea un'interfaccia del processore dati e carica la trama; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) crea l'interfaccia del processore dati.

Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.

Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

