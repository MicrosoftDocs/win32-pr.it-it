---
title: Proprietà Label IWMPCdromBurn
description: La proprietà Label ottiene la stringa dell'etichetta del volume CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- Proprietà etichetta Windows Media Player
- Proprietà Label Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, proprietà Label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329656"
---
# <a name="iwmpcdromburnlabel-property"></a>Proprietà IWMPCdromBurn:: Label

La proprietà *Label* ottiene la stringa dell'etichetta del volume CD.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che è la stringa dell'etichetta del volume.

## <a name="remarks"></a>Commenti

A causa del modo in cui vengono archiviate le etichette CD, l'etichetta del CD potrebbe essere inferiore alla lunghezza della stringa dell'etichetta di volume specificata. Se la stringa supera la lunghezza massima consentita per un'etichetta CD, il testo verrà troncato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





