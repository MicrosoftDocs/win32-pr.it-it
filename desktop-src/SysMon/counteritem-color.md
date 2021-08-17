---
title: CounterItem.Color - proprietà
description: Recupera o imposta il colore utilizzato per tracciare il valore del contatore.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Proprietà Color SysMon
- Proprietà Color SysMon , classe CounterItem
- Classe CounterItem SysMon , proprietà Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcc51862c57312f9b923ea6a80f9814182bbc6aef707dab994b135ace9637754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883869"
---
# <a name="counteritemcolor-property"></a>CounterItem.Color - proprietà

Recupera o imposta il colore utilizzato per tracciare il valore del contatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Valore proprietà

Colore usato per tracciare il valore del contatore.

## <a name="remarks"></a>Commenti

Se non si specifica il colore da usare, SYSMON seleziona i colori per i primi sedici contatori. Se si specificano più di sedici contatori, SYSMON riutilizzerà gli stessi colori dei primi sedici contatori. Per distinguere i contatori l'uno dall'altro, SYSMON modifica lo stile della linea usato per ogni multiplo di sedici contatori fino ai primi 80 contatori. [](counteritem-linestyle.md) Ad esempio, i primi sedici contatori usano uno stile linea continua, i sedici successivi usano uno stile linea tratteggiata e così via. SYSMON imposta quindi lo [**spessore**](counteritem-width.md) della riga su 2 per i contatori 81 - 96 e su 3 per i contatori 96 - 112. Se la raccolta contiene più di 112 contatori, i contatori conterranno valori duplicati di colore, stile di linea e larghezza.

**Prima di Windows Vista:** Se non si specifica il colore da usare, SYSMON seleziona i colori per i primi sedici contatori. Se si specificano più di sedici contatori, SYSMON riutilizzerà gli stessi colori dei primi sedici contatori. Per distinguere i contatori l'uno dall'altro, SYSMON aumenta la larghezza della riga dei primi tre contatori che ricevono la stessa assegnazione di colore. [](counteritem-width.md) Se più di tre contatori usano lo stesso colore, SYSMON sceglie in modo casuale lo spessore della linea da usare per il contatore.

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

 

 





