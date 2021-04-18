---
title: Proprietà SystemMonitor. Appearance
description: Recupera o imposta l'aspetto del controllo in modo da includere o omettere gli effetti di visualizzazione tridimensionali.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Proprietà Appearance SysMon
- Proprietà Appearance SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301064"
---
# <a name="systemmonitorappearance-property"></a>Proprietà SystemMonitor. Appearance

Recupera o imposta l'aspetto del controllo in modo da includere o omettere gli effetti di visualizzazione tridimensionali.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property Appearance As Long
```



## <a name="property-value"></a>Valore proprietà

Valore di aspetto che determina se il controllo viene disegnato con effetti tridimensionali.

È possibile impostare questa proprietà su uno dei valori seguenti.



| Valore                                                                        | Significato                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Disegna il controllo senza effetti visivi.<br/>                                    |
| <dl> <dt>1</dt> </dl> | Disegna il controllo con effetti tridimensionali. Si tratta del valore predefinito.<br/> |



 

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione               | Condizione                                    |
|------------------------------|----------------------------------------------|
| **System. ArgumentException** | Il valore dell'aspetto specificato non è valido. |



 

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di ambiente. Il valore di questa proprietà è determinato dal contenitore. L'impostazione del valore di questa proprietà potrebbe influire sull'illusione del controllo e del contenitore come una singola applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





