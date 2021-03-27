---
title: Funzione D3DX11GetImageInfoFromResource (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare le funzioni delle risorse, quindi utilizzare la libreria DirectXTex (strumenti), LoadFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Recupera le informazioni su una determinata immagine in una risorsa.
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
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982328"
---
# <a name="d3dx11getimageinfofromresource-function"></a>D3DX11GetImageInfoFromResource (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della [risorsa](/windows/desktop/menurc/resources-functions), quindi utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LOADFROMXXXMEMORY** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.

 

Recupera le informazioni su una determinata immagine in una risorsa.

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

*hSrcModule* \[ in\]
</dt> <dd>

Tipo: **[ **hmodule**](/windows/desktop/WinProg/windows-data-types)**

Modulo in cui viene caricata la risorsa. Impostare questo parametro su **null** per specificare il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.

</dd> <dt>

*pSrcResource* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a una stringa che specifica il nome del file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*pPump* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono. Può essere **null**. Vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> <dt>

*pSrcInfo* \[ in\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***

Puntatore a una \_ \_ struttura di informazioni sull'immagine D3DX11 per la compilazione con la descrizione dei dati nel file di origine.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **null**. Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in **D3DX11GetImageInfoFromResourceW**. In caso contrario, la chiamata di funzione viene risolta in **D3DX11GetImageInfoFromResourceA** perché vengono utilizzate le stringhe ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

