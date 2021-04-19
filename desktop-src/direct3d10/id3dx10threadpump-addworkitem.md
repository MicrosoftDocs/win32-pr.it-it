---
description: Aggiungere un elemento di lavoro alla pompa di thread.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'Metodo ID3DX10ThreadPump:: AddWorkItem (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323674"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a>Metodo ID3DX10ThreadPump:: AddWorkItem

Aggiungere un elemento di lavoro alla pompa di thread.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataLoader* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***

Caricatore che verrà utilizzato dal thread Pump quando un elemento di lavoro richiede il caricamento dei dati.

</dd> <dt>

*pDataProcessor* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***

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

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




