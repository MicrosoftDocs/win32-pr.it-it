---
title: Funzione D3DX11PreprocessShaderFromFile (D3DX11async.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota Invece di usare questa funzione, è consigliabile usare l'API D3DPreprocess. Creare uno shader da un file senza compilarlo.
ms.assetid: aab08efd-b6b0-44e5-bd68-f32c242d9e94
keywords:
- Funzione D3DX11PreprocessShaderFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ef5c7c9a00475ead0904cbf62d6d21fd647ce0de9fe402d1499dac7ee1bd09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124666"
---
# <a name="d3dx11preprocessshaderfromfile-function"></a>Funzione D3DX11PreprocessShaderFromFile

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Invece di usare questa funzione, è consigliabile usare l'API [**D3DPreprocess.**](/windows/desktop/direct3dhlsl/d3dpreprocess)

 

Creare uno shader da un file senza compilarlo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del file shader.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const D3D11 \_ SHADER \_ MACRO \***

Matrice con terminazione NULL di macro shader. impostare questa proprietà **su NULL** per non specificare macro.

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Puntatore a un'interfaccia di inclusione. impostare questa proprietà su **NULL** per specificare che non è presente alcun file di inclusione.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntatore a un'interfaccia pump di thread (vedere [**l'interfaccia ID3DX11ThreadPump).**](id3dx11threadpump.md) Usare **NULL** per specificare che questa funzione non deve restituire alcun valore finché non viene completata.

</dd> <dt>

*ppShaderText* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore alla memoria che contiene lo shader non ricompilato.

</dd> <dt>

*ppErrorMsgs* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un puntatore alla memoria che contiene gli eventuali errori di creazione dell'effetto.

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

