---
description: Impostare gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: Metodo ID3DX10ThreadPump::P rocessDeviceWorkItems (D3DX10.h)
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
ms.openlocfilehash: e7179cf285c056601d00df5126ba98aaa34f827cbcac15400166d8301dc143a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301777"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>Metodo ID3DX10ThreadPump::P rocessDeviceWorkItems

Impostare gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione. Al termine del caricamento e dell'elaborazione di una risorsa o di uno shader, il thread pump lo conterà in una coda fino a quando non viene chiamata questa API, a quel punto gli elementi elaborati verranno impostati sul dispositivo. Ciò è utile per controllare la quantità di elaborazione che viene spesa per associare le risorse al dispositivo per ogni frame. Vedere la sezione Osservazioni.

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di elementi di lavoro da impostare sul dispositivo. ProcessDeviceObjectCreation creerà al massimo oggetti iWorkItemCount. Se nella coda non sono presenti elementi di lavoro sufficienti per elaborare oggetti iWorkItemCount, ProcessDeviceObjectCreation creerà tutti gli oggetti dispositivo quanti sono gli elementi nella coda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Come esempio di come si potrebbe usare questa API, si supponga di essere vicini alla fine di un livello nel gioco e di voler iniziare a precaricare trame, shader e altre risorse per il livello successivo. Il thread pump inizierà a caricare, decomprimere ed elaborare le risorse e gli shader in un thread separato fino a quando non saranno pronti per essere impostati sul dispositivo, a quel punto li lascerà in una coda. È possibile che non si voglia impostare tutte le risorse e gli shader sul dispositivo contemporaneamente, perché ciò potrebbe causare un rallentamento temporaneo delle prestazioni del gioco. Questa API può quindi essere chiamata una volta per ogni frame in modo che solo un numero ridotto di elementi di lavoro sia impostato sul dispositivo in ogni frame, stendendo così il carico di lavoro delle risorse di associazione al dispositivo su più frame e riducendo al minimo la possibilità di un rallentamento notabile nelle prestazioni del gioco.

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

 

 
