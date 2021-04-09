---
title: Proprietà CounterItem. Width
description: Recupera o imposta la lunghezza riga utilizzata per rappresentare il valore del contatore.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Proprietà Width SysMon
- Proprietà Width SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà Width
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
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741786"
---
# <a name="counteritemwidth-property"></a>Proprietà CounterItem. Width

Recupera o imposta la lunghezza riga utilizzata per rappresentare il valore del contatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property Width As Long
```



## <a name="property-value"></a>Valore proprietà

Spessore riga utilizzato in un grafico a linee. I valori validi sono compresi tra 1 e 3, dove 1 (il valore predefinito) è la larghezza più stretta.

**Prima di Windows Vista:** I valori validi sono compresi tra 1 e 9. Se l'applicazione verrà eseguita in Windows Vista, non utilizzare un valore di larghezza maggiore di 3.

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione               | Condizione                              |
|------------------------------|----------------------------------------|
| **System. ArgumentException** | Lunghezza riga specificata non valida. |



 

## <a name="remarks"></a>Commenti

La lunghezza di riga predefinita per i primi sedici contatori aggiunti è 1. La lunghezza di riga predefinita per i successivi sedici contatori (contatori 17-32) aggiunti è 2. La lunghezza di riga predefinita per i successivi sedici contatori (contatori 33-48) aggiunta è 3. Successivamente, SYSMON sceglie in modo casuale la lunghezza della linea. Per informazioni dettagliate, vedere [**CounterItem. Color**](counteritem-color.md).

Per specificare uno [**stile di linea**](counteritem-linestyle.md) diverso da Solid, la larghezza deve essere 1. Se si specifica un valore maggiore di 1 e si specifica uno stile di linea non a tinta unita, SYSMON ignora la lunghezza di riga specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





