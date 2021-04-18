---
title: Proprietà CounterItem. ScaleFactor
description: Recupera o imposta il fattore di scala utilizzato per rappresentare il valore del contatore.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Proprietà ScaleFactor SysMon
- Proprietà ScaleFactor SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà ScaleFactor
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
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301750"
---
# <a name="counteritemscalefactor-property"></a>Proprietà CounterItem. ScaleFactor

Recupera o imposta il fattore di scala utilizzato per rappresentare il valore del contatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Valore proprietà

Fattore di scala utilizzato per visualizzare i valori dei contatori grafici. I valori validi sono compresi tra-9 e 9 (i valori corrispondono a 0,000000001-100000000,0).

**Prima di Windows Vista:** I valori validi sono compresi tra-7 e 7 (i valori corrispondono a 0,0000001-1000000,0).

## <a name="remarks"></a>Commenti

Impostare questa proprietà solo se si desidera modificare il fattore di scala predefinito del contatore. ogni contatore definisce il proprio fattore di scala. Il valore di questa proprietà è impostato su Integer. MaxValue se il contatore usa il fattore di scala predefinito per rappresentare i valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**SystemMonitor. ScaleToFit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





