---
title: Funzione D3DX11GetImageInfoFromResource (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota Invece di usare questa funzione, è consigliabile usare le funzioni di risorsa, quindi usare la libreria DirectXTex (strumenti), LoadFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi. Recupera informazioni su una determinata immagine in una risorsa.
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- Funzione D3DX11GetImageInfoFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ada8118dac3e39f9f91012bb3ec681db7b156540cffae0fb7c0f1a7bc1819b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535956"
---
# <a name="d3dx11getimageinfofromresource-function"></a>Funzione D3DX11GetImageInfoFromResource

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché usare questa funzione, è consigliabile usare le funzioni di risorsa [,](/windows/desktop/menurc/resources-functions)quindi usare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LoadFromXXXMemory** (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi.

 

Recupera informazioni su una determinata immagine in una risorsa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Modulo in cui viene caricata la risorsa. Impostare questo parametro su **NULL** per specificare il modulo associato all'immagine usata dal sistema operativo per creare il processo corrente.

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a una stringa che specifica il nome file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono. Può essere **NULL.** Vedere [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).

</dd> <dt>

*pSrcInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

Puntatore a una struttura D3DX11 IMAGE INFO da riempire con la descrizione dei \_ dati nel file di \_ origine.

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere un percorso di memoria valido fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in **D3DX11GetImageInfoFromResourceW**. In caso contrario, la chiamata di funzione viene risolta **in D3DX11GetImageInfoFromResourceA** perché vengono usate stringhe ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

