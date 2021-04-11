---
description: Impostare gli elementi di lavoro sul dispositivo dopo aver completato il caricamento e l'elaborazione.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: Metodo ID3DX10ThreadPump::P rocessDeviceWorkItems (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132415"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>ID3DX10ThreadPump::P metodo rocessDeviceWorkItems

Impostare gli elementi di lavoro sul dispositivo dopo aver completato il caricamento e l'elaborazione. Al termine del caricamento e dell'elaborazione di una risorsa o di uno shader, il thread Pump lo manterrà in una coda fino a quando non viene chiamata l'API, a quel punto gli elementi elaborati verranno impostati sul dispositivo. Questa operazione è utile per controllare la quantità di elaborazione dedicata al binding delle risorse al dispositivo per ogni frame. Vedere la sezione Osservazioni.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di elementi di lavoro da impostare sul dispositivo. ProcessDeviceObjectCreation creerà al massimo oggetti iWorkItemCount. Se nella coda non sono presenti elementi di lavoro sufficienti per elaborare gli oggetti iWorkItemCount, ProcessDeviceObjectCreation creerà un numero di oggetti dispositivo pari a quello degli elementi della coda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Come esempio di come è possibile usare questa API, è possibile che si stia avvicinando alla fine di un livello del gioco e si voglia iniziare a precaricare le trame, gli shader e altre risorse per il livello successivo. Il pump di thread inizierà a caricare, decomprimere ed elaborare le risorse e gli shader in un thread separato fino a quando non saranno pronti per essere impostati sul dispositivo, a quel punto li lascerà in una coda. È possibile che non si desideri impostare contemporaneamente tutte le risorse e gli shader per il dispositivo, perché ciò può causare un rallentamento momentaneo evidente nelle prestazioni del gioco. Questa API potrebbe quindi essere chiamata una volta per ogni fotogramma, in modo che solo un numero ridotto di elementi di lavoro venga impostato sul dispositivo in ogni frame, in modo da distribuire il carico di lavoro delle risorse di associazione al dispositivo su diversi frame e ridurre al minimo la possibilità di un rallentamento evidente nelle prestazioni del gioco.

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

 

 
