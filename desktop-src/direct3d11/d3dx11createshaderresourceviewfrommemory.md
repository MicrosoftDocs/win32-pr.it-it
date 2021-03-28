---
title: Funzione D3DX11CreateShaderResourceViewFromMemory (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTK (Runtime), CreateXXXTextureFromMemory (dove XXX è DDS o WIC) DirectXTex Library (Tools), LoadFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi CreateShaderResourceView crea una visualizzazione risorse shader da un file in memoria.
ms.assetid: fd75b187-2c9c-403c-8327-c312c4cda238
keywords:
- Funzione D3DX11CreateShaderResourceViewFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0730fafdeb85cc22944f282eaaf556a1cdb12d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996008"
---
# <a name="d3dx11createshaderresourceviewfrommemory-function"></a>D3DX11CreateShaderResourceViewFromMemory (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:
>
> -   Libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (dove xxx è DDS o WIC)
> -   Libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LOADFROMXXXMEMORY** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi **CreateShaderResourceView**

 

Creare una visualizzazione risorse shader da un file in memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateShaderResourceViewFromMemory(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Un puntatore al dispositivo (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) che utilizzerà la risorsa.

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Puntatore al file in memoria che contiene la visualizzazione delle risorse dello shader.

</dd> <dt>

*SrcDataSize* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Dimensioni del file in memoria.

</dd> <dt>

*pLoadInfo* \[ in\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.

</dd> <dt>

*pPump* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)). Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.

</dd> <dt>

*ppShaderResourceView* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Indirizzo di un puntatore alla visualizzazione delle risorse dello shader appena creata. Vedere [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **null**. Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

