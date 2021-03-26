---
title: Metodo ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Imposta gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Metodo ProcessDeviceWorkItems Direct3D 11
- Metodo ProcessDeviceWorkItems Direct3D 11, interfaccia ID3DX11ThreadPump
- Interfaccia ID3DX11ThreadPump Direct3D 11, metodo ProcessDeviceWorkItems
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
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982226"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>ID3DX11ThreadPump::P metodo rocessDeviceWorkItems

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

*iWorkItemCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi di lavoro da impostare sul dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Al termine del caricamento e dell'elaborazione di una risorsa o di uno shader, il thread Pump lo manterrà in una coda fino a quando non viene chiamata l'API, a quel punto gli elementi elaborati verranno impostati sul dispositivo. Questa operazione è utile per controllare la quantità di elaborazione dedicata al binding delle risorse al dispositivo per ogni frame.

Come esempio di come è possibile usare questa API, è possibile che si stia avvicinando alla fine di un livello del gioco e si voglia iniziare a precaricare le trame, gli shader e altre risorse per il livello successivo. Il pump di thread inizierà a caricare, decomprimere ed elaborare le risorse e gli shader in un thread separato fino a quando non saranno pronti per essere impostati sul dispositivo, a quel punto li lascerà in una coda. È possibile che non si desideri impostare contemporaneamente tutte le risorse e gli shader per il dispositivo, perché ciò può causare un rallentamento temporaneo evidente nelle prestazioni del gioco. Questa API potrebbe quindi essere chiamata una volta per ogni fotogramma, in modo che solo un numero ridotto di elementi di lavoro venga impostato sul dispositivo in ogni frame, distribuendo in tal modo il carico di lavoro delle risorse di associazione al dispositivo su diversi frame.

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

 

