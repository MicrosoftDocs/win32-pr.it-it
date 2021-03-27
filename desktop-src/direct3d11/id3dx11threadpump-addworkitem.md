---
title: Metodo ID3DX11ThreadPump AddWorkItem (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Aggiunge un elemento di lavoro alla pompa di thread.
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Metodo AddWorkItem Direct3D 11
- Metodo AddWorkItem Direct3D 11, interfaccia ID3DX11ThreadPump
- Interfaccia ID3DX11ThreadPump Direct3D 11, metodo AddWorkItem
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354274"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a>Metodo ID3DX11ThreadPump:: AddWorkItem

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Aggiunge un elemento di lavoro alla pompa di thread.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataLoader* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***

Caricatore che verrà utilizzato dal thread Pump quando un elemento di lavoro richiede il caricamento dei dati.

</dd> <dt>

*pDataProcessor* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***

Processore che verrà utilizzato dal thread Pump quando un elemento di lavoro richiede l'elaborazione dei dati.

</dd> <dt>

*pHResult* \[ in\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **null**.

</dd> <dt>

*ppDeviceObject* \[ out\]
</dt> <dd>

Tipo: **void \* \***

Dispositivo che usa l'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





