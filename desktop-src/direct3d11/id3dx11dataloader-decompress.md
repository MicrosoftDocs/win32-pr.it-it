---
title: Metodo Decompress ID3DX11DataLoader (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Decomprime i dati codificati.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Decomprimi metodo Direct3D 11
- Decomprimi metodo Direct3D 11, interfaccia ID3DX11DataLoader
- Interfaccia ID3DX11DataLoader Direct3D 11, metodo Decompress
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969512"
---
# <a name="id3dx11dataloaderdecompress-method"></a>ID3DX11DataLoader::D Metodo eComPress

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Decomprime i dati codificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **void \* \***

Puntatore ai dati non elaborati da decomprimere.

</dd> <dt>

*pcBytes* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)\***

Dimensione dei dati a cui punta ppData.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per caricare le risorse da file System, ad esempio file ZIP. Quando si esegue il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.

L' [**interfaccia ID3DX11DataLoader**](id3dx11dataloader.md) può essere ereditata e i membri ridefiniti per supportare i formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

