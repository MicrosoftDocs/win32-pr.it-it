---
title: Funzione D3DX11CreateTextureFromMemory (D3DX11.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota Invece di usare questa funzione, è consigliabile usare queste librerie DirectXTK (runtime), CreateXXXTextureFromMemory (dove XXX è DDS o WIC)Libreria DirectXTex (strumenti), LoadFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi CreateTexture Crea una risorsa trama da un file che risiede nella memoria di sistema.
ms.assetid: 1b07653e-8dc8-40b2-b591-bd25a54cfaa2
keywords:
- Funzione D3DX11CreateTextureFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17ed4fb842d3a14ed1f8bde2e9371c134e98ba61a54cbde32c98b7fe3939bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099587"
---
# <a name="d3dx11createtexturefrommemory-function"></a>Funzione D3DX11CreateTextureFromMemory

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Invece di usare questa funzione, è consigliabile usare:
>
> -   [Libreria DirectXTK](https://github.com/Microsoft/DirectXTK) (runtime), **CreateXXXTextureFromMemory** (dove XXX è DDS o WIC)
> -   [Libreria DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LoadFromXXXMemory** (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi **CreateTexture**

 

Creare una risorsa trama da un file che risiede nella memoria di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateTextureFromMemory(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntatore al dispositivo (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) che userà la risorsa.

</dd> <dt>

*pSrcData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Puntatore alla risorsa nella memoria di sistema.

</dd> <dt>

*SrcDataSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Dimensioni della risorsa nella memoria di sistema.

</dd> <dt>

*pLoadInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)) quando viene creato il processore di dati. Impostare questa proprietà su **NULL** per leggere le caratteristiche di una trama quando la trama viene caricata.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntatore a un'interfaccia pump di thread (vedere [**l'interfaccia ID3DX11ThreadPump).**](id3dx11threadpump.md) Se si specifica **NULL,** questa funzione si comporterà in modo sincrono e non restituirà un valore finché non viene completata.

</dd> <dt>

*ppTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***

Indirizzo di un puntatore alla risorsa creata. Vedere [**ID3D11Resource.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)

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
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

