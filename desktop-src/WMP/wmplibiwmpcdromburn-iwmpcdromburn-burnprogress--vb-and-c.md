---
title: Proprietà burnProgress di IWMPCdromBurn
description: La proprietà burnProgress ottiene lo stato di avanzamento del CD come percentuale di completamento.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- Finestra delle proprietà di burnProgress Media Player
- Proprietà di burnProgress Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, proprietà burnProgress
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329669"
---
# <a name="iwmpcdromburnburnprogress-property"></a>Proprietà IWMPCdromBurn:: burnProgress

La proprietà **burnProgress** ottiene lo stato di avanzamento del CD come percentuale di completamento.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il valore di avanzamento. I valori di avanzamento sono compresi tra 0 e 100.

## <a name="remarks"></a>Commenti

Il valore di avanzamento rappresenta la percentuale completa dell'intero processo di masterizzazione, incluse le operazioni di gestione temporanea.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





