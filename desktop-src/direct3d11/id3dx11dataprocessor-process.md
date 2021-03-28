---
title: Metodo di elaborazione ID3DX11DataProcessor (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Elabora i dati.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Metodo di elaborazione Direct3D 11
- Metodo di elaborazione Direct3D 11, interfaccia ID3DX11DataProcessor
- Interfaccia ID3DX11DataProcessor Direct3D 11, metodo Process
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530949"
---
# <a name="id3dx11dataprocessorprocess-method"></a>ID3DX11DataProcessor::P metodo rocess

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Elabora i dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Tipo: **void \***

Puntatore ai dati da elaborare.

</dd> <dt>

*cBytes* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Dimensione dei dati da elaborare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Questo metodo viene utilizzato da un' [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

