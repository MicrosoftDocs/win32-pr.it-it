---
description: Aggiungere un elemento di lavoro al thread pump.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: Metodo ID3DX10ThreadPump::AddWorkItem (D3DX10.h)
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
ms.openlocfilehash: 43602019018a9751453eb93f4ffb9b1c29eada6caf120a6721522982c3355dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609321"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a>Metodo ID3DX10ThreadPump::AddWorkItem

Aggiungere un elemento di lavoro al thread pump.

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

*pDataLoader* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***

Caricatore che verrà utilizzato dal thread pump quando un elemento di lavoro richiede il caricamento dei dati.

</dd> <dt>

*pDataProcessor* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***

Processore che verrà utilizzato dal thread pump quando un elemento di lavoro richiede l'elaborazione dei dati.

</dd> <dt>

*pHResult* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.**

</dd> <dt>

*ppDeviceObject* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* void**

Dispositivo che usa l'oggetto .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




