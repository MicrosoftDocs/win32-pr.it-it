---
title: Proprietà etichetta IWMPCdromBurn
description: La proprietà label ottiene la stringa dell'etichetta del volume CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- proprietà label Windows Media Player
- proprietà label Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player , proprietà label
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
ms.openlocfilehash: d8b8917706e20b5d1361054ac5f6fd209c0026837c428ecba715727e3d828a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000550"
---
# <a name="iwmpcdromburnlabel-property"></a>Proprietà IWMPCdromBurn::label

La *proprietà label* ottiene la stringa dell'etichetta del volume CD.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.String che** rappresenta la stringa dell'etichetta di volume.

## <a name="remarks"></a>Commenti

A causa della modalità di archiviazione delle etichette CD, l'etichetta del CD può essere più breve della lunghezza della stringa di etichetta di volume specificata. Se la stringa è più lunga della lunghezza massima di un'etichetta CD, il testo verrà troncato.

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

 

 





