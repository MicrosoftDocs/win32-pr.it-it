---
title: CounterItem.Width - proprietà
description: Recupera o imposta lo spessore della linea utilizzato per tracciare il valore del contatore.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Proprietà Width SysMon
- Proprietà Width SysMon , classe CounterItem
- Classe CounterItem SysMon , proprietà Width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5deca3d7fa188c834f2ca952c9b6c4760a3a1b56c83eb8250e343257b8108de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883507"
---
# <a name="counteritemwidth-property"></a>CounterItem.Width - proprietà

Recupera o imposta lo spessore della linea utilizzato per tracciare il valore del contatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property Width As Long
```



## <a name="property-value"></a>Valore proprietà

Spessore della linea usato in un grafico a linee. I valori validi sono da 1 a 3, dove 1 (il valore predefinito) è la larghezza più stretta.

**Prima di Windows Vista:** I valori validi sono da 1 a 9. Non usare un valore di larghezza maggiore di 3 se l'applicazione verrà eseguita in Windows Vista.

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione               | Condizione                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | Lo spessore di riga specificato non è valido. |



 

## <a name="remarks"></a>Commenti

Lo spessore di riga predefinito per i primi sedici contatori aggiunti è 1. Lo spessore di riga predefinito per i sedici contatori successivi (contatori da 17 a 32) aggiunti è 2. Lo spessore di riga predefinito per i sedici contatori successivi (contatori da 33 a 48) aggiunti è 3. Successivamente, SYSMON sceglie in modo casuale lo spessore della linea. Per informazioni dettagliate, [**vedere CounterItem.Color.**](counteritem-color.md)

Per specificare uno [**stile di linea**](counteritem-linestyle.md) diverso da tinta unita, lo spessore deve essere 1. Se si specifica un valore maggiore di 1 e si specifica uno stile di linea non continua, SYSMON ignora lo spessore di riga specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





