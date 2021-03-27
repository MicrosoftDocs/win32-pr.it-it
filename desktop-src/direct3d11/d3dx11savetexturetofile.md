---
title: Funzione D3DX11SaveTextureToFile (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, CaptureTexture quindi SaveToXXXFile (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Per lo scenario semplificato della creazione di una schermata da una trama di destinazione di rendering, è consigliabile usare la libreria DirectXTK, SaveDDSTextureToFile o SaveWICTextureToFile. Salva una trama in un file.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- Funzione D3DX11SaveTextureToFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982316"
---
# <a name="d3dx11savetexturetofile-function"></a>D3DX11SaveTextureToFile (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** quindi **SAVETOXXXFILE** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Per lo scenario semplificato della creazione di una schermata da una trama di destinazione di rendering, è consigliabile usare la libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SaveDDSTextureToFile** o **SaveWICTextureToFile**.

 

Salva una trama in un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*pSrcTexture* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Puntatore alla trama da salvare. Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*DestFormat* \[ in\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**

Il formato in cui verrà salvata la trama (vedere il [**\_ formato del \_ file \_ di immagine D3DX11**](d3dx11-image-file-format.md)). D3DX11 \_ IFF \_ DDS è il formato preferito perché è l'unica opzione che supporta tutti i formati nel [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del file di output di destinazione in cui verrà salvata la trama. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Direct3D 11 Return code](d3d11-graphics-reference-returnvalues.md); usare il valore restituito per verificare se il *DestFormat* è supportato.

## <a name="remarks"></a>Commenti

**D3DX11SaveTextureToFile** scrive la struttura [**DXT10 dell' \_ intestazione \_ DDS**](/windows/desktop/direct3ddds/dds-header-dxt10) aggiuntiva per la trama di input solo se necessario, ad esempio perché la trama di input è in formato RGB standard. Se **D3DX11SaveTextureToFile** scrive l' **intestazione DDS \_ \_ DXT10** structure, imposta il membro **dwFourCC** della struttura [**DDS \_ PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) per la trama su **DX10** per indicare la prescense dell'intestazione **DDS \_ \_ DXT10** Extended header.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

