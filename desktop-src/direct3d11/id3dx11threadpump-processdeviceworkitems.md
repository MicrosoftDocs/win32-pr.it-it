---
title: Metodo ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Imposta gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Metodo ProcessDeviceWorkItems Direct3D 11
- Metodo ProcessDeviceWorkItems Direct3D 11, interfaccia ID3DX11ThreadPump
- ID3DX11ThreadPump interface Direct3D 11 , ProcessDeviceWorkItems method
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a6918e9ecea9d66c3ebca034628387ea471e9173b4b14f24e9b7f866897325
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608671"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>Metodo ID3DX11ThreadPump::P rocessDeviceWorkItems

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Imposta gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iWorkItemCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi di lavoro da impostare sul dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Al termine del caricamento e dell'elaborazione di una risorsa o di uno shader, il thread pump lo conterà in una coda fino a quando non viene chiamata questa API, a quel punto gli elementi elaborati verranno impostati sul dispositivo. Ciò è utile per controllare la quantità di elaborazione che viene impiegato per associare le risorse al dispositivo per ogni frame.

Come esempio di come si potrebbe usare questa API, si supponga di essere prossimi alla fine di un livello nel gioco e di voler iniziare a precaricare le trame, gli shader e altre risorse per il livello successivo. Il thread pump inizierà a caricare, decomprimere ed elaborare le risorse e gli shader in un thread separato fino a quando non saranno pronti per essere impostati sul dispositivo, a quel punto li lascerà in una coda. È possibile che non si vogliano impostare contemporaneamente tutte le risorse e gli shader sul dispositivo, perché ciò potrebbe causare un notevole rallentamento temporaneo delle prestazioni del gioco. È quindi possibile chiamare questa API una volta per ogni frame in modo che solo un numero ridotto di elementi di lavoro sia impostato sul dispositivo in ogni fotogramma, stendendo così il carico di lavoro delle risorse di binding al dispositivo su più frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

