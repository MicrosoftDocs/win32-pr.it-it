---
title: Funzione D3DX11GetImageInfoFromMemory (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, GetMetadataFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Ottenere informazioni su un'immagine già caricata in memoria.
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- Funzione D3DX11GetImageInfoFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5f1f04c9540614541b9f63b7833967d6ce959
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982325"
---
# <a name="d3dx11getimageinfofrommemory-function"></a>D3DX11GetImageInfoFromMemory (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GETMETADATAFROMXXXMEMORY** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.

 

Ottenere informazioni su un'immagine già caricata in memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Puntatore all'immagine in memoria.

</dd> <dt>

*SrcDataSize* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Dimensione dell'immagine in memoria, in byte.

</dd> <dt>

*pPump* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono. Può essere **null**. Vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> <dt>

*pSrcInfo* \[ in\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***

Informazioni sull'immagine in memoria.

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

 

