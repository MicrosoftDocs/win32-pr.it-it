---
title: Metodo ID3DX11ThreadPump GetQueueStatus (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Ottiene il numero di elementi in ognuna delle tre code all'interno della pompa di thread.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Metodo GetQueueStatus Direct3D 11
- Metodo GetQueueStatus Direct3D 11, interfaccia ID3DX11ThreadPump
- Interfaccia ID3DX11ThreadPump Direct3D 11, metodo GetQueueStatus
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982232"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a>Metodo ID3DX11ThreadPump:: GetQueueStatus

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Ottiene il numero di elementi in ognuna delle tre code all'interno della pompa di thread.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIoQueue* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Numero di elementi nella coda di I/O.

</dd> <dt>

*pProcessQueue* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Numero di elementi nella coda dei processi.

</dd> <dt>

*pDeviceQueue* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Numero di elementi nella coda del dispositivo.

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

 

