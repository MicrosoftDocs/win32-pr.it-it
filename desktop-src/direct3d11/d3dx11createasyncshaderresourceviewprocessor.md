---
title: Funzione D3DX11CreateAsyncShaderResourceViewProcessor (D3DX11async.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- Funzione D3DX11CreateAsyncShaderResourceViewProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305705a4fd82b7f2267e3d56630b78c8c8d98473d946b1629e713162f4a6ae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536570"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a>Funzione D3DX11CreateAsyncShaderResourceViewProcessor

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.

 

Creare un processore di dati che carica una risorsa e quindi creare una vista shader-risorsa per essa. I data processor sono un componente della funzionalità di caricamento dati asincrono in D3DX11 che usa [**le pompe di thread**](id3dx11threadpump.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntatore al dispositivo Direct3D (vedere [**ID3D11Device)**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)che verrà usato per creare una risorsa e una visualizzazione shader-risorsa per tale risorsa.

</dd> <dt>

*pLoadInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)) quando viene creato il processore di dati. Impostare questo valore su **NULL** per leggere le caratteristiche di una trama quando la trama viene caricata.

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

Non esiste alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.

Per Windows app di Store, gli esempi DirectX (ad esempio, l'esempio di esercitazione [Direct3D)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Per le app desktop Win32, è possibile usare il runtime di concorrenza [per](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) implementare qualcosa di simile al modello di programmazione asincrona Windows Runtime.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

