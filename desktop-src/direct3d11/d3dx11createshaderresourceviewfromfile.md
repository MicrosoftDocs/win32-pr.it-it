---
title: Funzione D3DX11CreateShaderResourceViewFromFile (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota Invece di usare questa funzione, è consigliabile usare queste librerie DirectXTK (runtime), CreateXXXTextureFromFile (dove XXX è DDS o WIC)Libreria DirectXTex (strumenti), LoadFromXXXFile (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi CreateShaderResourceView Crea una visualizzazione shader-risorsa da un file.
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- Funzione D3DX11CreateShaderResourceViewFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6862b5008ed74687e30a9f233e3544ecd69719a20cdcb3f4dd9409de31f6d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124746"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a>Funzione D3DX11CreateShaderResourceViewFromFile

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.

 

> [!Note]  
> Invece di usare questa funzione, è consigliabile usare:
>
> -   [Libreria DirectXTK](https://github.com/Microsoft/DirectXTK) (runtime), **CreateXXXTextureFromFile** (dove XXX è DDS o WIC)
> -   [Libreria DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LoadFromXXXFile** (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi **CreateShaderResourceView**

 

Creare una visualizzazione shader-risorsa da un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntatore al dispositivo (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) che userà la risorsa.

</dd> <dt>

*pSrcFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del file che contiene la visualizzazione shader-risorsa. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> <dt>

*pLoadInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)) quando viene creato il processore di dati. Impostare questa proprietà su **NULL** per leggere le caratteristiche di una trama quando la trama viene caricata.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntatore a un'interfaccia thread-pump (vedere [**l'interfaccia ID3DX11ThreadPump).**](id3dx11threadpump.md) Se si specifica **NULL,** questa funzione si comporterà in modo sincrono e non restituirà un valore finché non viene completata.

</dd> <dt>

*ppShaderResourceView* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Indirizzo di un puntatore alla visualizzazione shader-risorsa (vedere [**ID3D11ShaderResourceView).**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Per un elenco dei formati di immagine supportati, vedere [**D3DX11 \_ IMAGE \_ FILE \_ FORMAT**](d3dx11-image-file-format.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

