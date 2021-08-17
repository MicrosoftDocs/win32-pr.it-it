---
title: CounterItem.ScaleFactor - proprietà
description: Recupera o imposta il fattore di scala utilizzato per tracciare il valore del contatore.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Proprietà ScaleFactor SysMon
- Proprietà ScaleFactor SysMon , classe CounterItem
- Classe CounterItem SysMon , proprietà ScaleFactor
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794cd84dd62518cc3089b8644f41b5545aeaf547b275c703a4cb87f5fec2b4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883666"
---
# <a name="counteritemscalefactor-property"></a>CounterItem.ScaleFactor - proprietà

Recupera o imposta il fattore di scala utilizzato per tracciare il valore del contatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Valore proprietà

Fattore di scala usato nella visualizzazione dei valori dei contatori con grafico. I valori validi sono da -9 a 9 (i valori corrispondono a 0,000000001 - 1000000000,0).

**Prima di Windows Vista:** I valori validi sono da -7 a 7 (i valori corrispondono a 0,00000001 - 10000000,0).

## <a name="remarks"></a>Commenti

Impostare questa proprietà solo se si vuole modificare il fattore di scala predefinito del contatore (ogni contatore definisce il proprio fattore di scala). Il valore di questa proprietà è impostato su Integer.MaxValue se il contatore usa il fattore di scala predefinito per tracciare i valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**SystemMonitor.ScaleToFit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





