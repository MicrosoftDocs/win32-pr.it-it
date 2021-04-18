---
title: Proprietà ripProgress di IWMPCdromRip
description: La proprietà ripProgress ottiene lo stato di ripping del CD come percentuale di completamento.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- Finestra delle proprietà di ripProgress Media Player
- Proprietà di ripProgress Media Player Windows, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip Windows Media Player, proprietà ripProgress
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329288"
---
# <a name="iwmpcdromripripprogress-property"></a>Proprietà IWMPCdromRip:: ripProgress

La proprietà **ripProgress** ottiene lo stato di ripping del CD come percentuale di completamento.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il valore di avanzamento. I valori di avanzamento sono compresi tra 0 e 100.

## <a name="remarks"></a>Commenti

Il valore di avanzamento rappresenta la percentuale completa dell'intero processo di estrazione. Per determinare lo stato di avanzamento di una traccia specifica, usare [IWMPMedia. GetItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) con **RipProgress** come nome dell'attributo. Per ottenere l'indice della traccia attualmente in fase di ripping, chiamare IWMPPlaylist. getItemInfo con "CurrentRipTrackIndex" come nome dell'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Copia di un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





