---
title: Funzione D3DX11GetImageInfoFromFile (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, GetMetadataFromXXXFile (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Recupera le informazioni su un file di immagine specificato.
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- Funzione D3DX11GetImageInfoFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058650"
---
# <a name="d3dx11getimageinfofromfile-function"></a>D3DX11GetImageInfoFromFile (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GETMETADATAFROMXXXFILE** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.

 

Recupera le informazioni su un file di immagine specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome file dell'immagine di cui recuperare le informazioni. Se \_ sono definiti Unicode o Unicode, questo tipo di parametro è LPCWSTR; in caso contrario, il tipo è LPCSTR.

</dd> <dt>

*pPump* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono. Può essere **null**. Vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> <dt>

*pSrcInfo* \[ in\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***

Puntatore a un [**oggetto \_ D3DX11 \_ informazioni sull'immagine**](d3dx11-image-info.md) da compilare con la descrizione dei dati nel file di origine.

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

Questa funzione supporta le stringhe Unicode e ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

