---
description: Salva una trama in un file.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Funzione D3DX10SaveTextureToFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323739"
---
# <a name="d3dx10savetexturetofile-function"></a>D3DX10SaveTextureToFile (funzione)

Salva una trama in un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcTexture* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntatore alla trama da salvare. Vedere [**interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*DestFormat* \[ in\]
</dt> <dd>

Tipo: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**

Il formato in cui verrà salvata la trama (vedere il [**\_ formato del \_ file \_ di immagine d3dx10**](d3dx10-image-file-format.md)). D3DX10 \_ IFF \_ DDS è il formato preferito perché è l'unica opzione che supporta tutti i formati nel [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome del file di output di destinazione in cui verrà salvata la trama. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 10](d3d10-graphics-reference-returnvalues.md); usare il valore restituito per verificare se il *DestFormat* è supportato.

## <a name="remarks"></a>Commenti

**D3DX10SaveTextureToFile** scrive la struttura [**DXT10 dell' \_ intestazione \_ DDS**](../direct3ddds/dds-header-dxt10.md) aggiuntiva per la trama di input solo se necessario, ad esempio perché la trama di input è in formato RGB standard. Se **D3DX10SaveTextureToFile** scrive l' **intestazione DDS \_ \_ DXT10** structure, imposta il membro **dwFourCC** della struttura [**DDS \_ PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) per la trama su **DX10** per indicare la prescense dell'intestazione **DDS \_ \_ DXT10** Extended header.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
