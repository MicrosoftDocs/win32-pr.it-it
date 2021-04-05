---
title: Proprietà SystemMonitor. Highlight
description: Recupera o imposta un valore che indica se i valori dei contatori selezionati sono evidenziati nel grafico.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Evidenziare la proprietà SysMon
- Highlight Property SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà Highlight
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873845"
---
# <a name="systemmonitorhighlight-property"></a>Proprietà SystemMonitor. Highlight

Recupera o imposta un valore che indica se i valori dei contatori selezionati sono evidenziati nel grafico.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a>Valore proprietà

True indica che i valori dei contatori selezionati sono evidenziati nel grafico; in caso contrario, false. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Per selezionare uno o più contatori, è possibile impostare [**CounterItem. Selected**](counteritem-selected.md) su true oppure l'utente può selezionare i contatori dall'elenco dei contatori visualizzati nella legenda.

**Prima di Windows Vista:** Non è possibile selezionare i contatori a livello di codice e l'utente può selezionare un solo contatore dall'elenco dei contatori visualizzati nella legenda.

L'evidenziazione può essere nera o bianca, a seconda del valore della proprietà [**BackColor**](systemmonitor-backcolor.md) . L'evidenziazione viene impostata automaticamente sul colore che fornirà un contrasto sufficiente tra il colore di evidenziazione e il colore di sfondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem. Selected**](counteritem-selected.md)
</dt> </dl>

 

 





