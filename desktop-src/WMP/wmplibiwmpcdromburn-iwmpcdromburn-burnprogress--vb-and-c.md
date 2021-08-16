---
title: Proprietà IWMPCdrom BurnProgress
description: La proprietà burnProgress ottiene lo stato di avanzamento della masterizzazione cd come percentuale di completamento.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- proprietà burnProgress Windows Media Player
- proprietà burnProgress Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdrom Burn Windows Media Player , proprietà burnProgress
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
ms.openlocfilehash: 90b8e468bc57bb40d990c0b2aeaffc23e184ef2ffa04ab85c9f60cf0d6bced57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332065"
---
# <a name="iwmpcdromburnburnprogress-property"></a>Proprietà IWMPCdromBurn::burnProgress

La **proprietà burnProgress** ottiene lo stato di avanzamento della masterizzazione cd come percentuale di completamento.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Int32** che rappresenta il valore di stato. I valori di stato sono da 0 a 100.

## <a name="remarks"></a>Commenti

Il valore di stato rappresenta la percentuale completata dell'intero processo di masterizzazione, incluse le operazioni di staging.

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

 

 





