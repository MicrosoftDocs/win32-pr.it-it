---
title: Evento SystemMonitor.OnDblClick
description: Notifica quando un utente fa doppio clic sulla linea del grafico, sulla barra dell'istogramma o sull'elemento del report con il pulsante sinistro del mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- SysMon dell'evento OnDblClick
- Evento OnDblClick SysMon , classe SystemMonitor
- Classe SystemMonitor SysMon , evento OnDblClick
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef829fad368e7d8cf3b65ab70db4600f6d635b1d36bcc5e3f50fcdbaf429a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883961"
---
# <a name="systemmonitorondblclick-event"></a>Evento SystemMonitor.OnDblClick

Notifica quando un utente fa doppio clic sulla linea del grafico, sulla barra dell'istogramma o sull'elemento del report con il pulsante sinistro del mouse.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ in, out\]
</dt> <dd>

Indice del contatore selezionato [**nell'oggetto raccolta Counters.**](counters.md) Se non è stato selezionato alcun contatore, viene restituito un valore di indice pari a 0. In caso contrario, viene restituito l'indice del contatore selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando viene attivato questo evento, nel riquadro Legenda viene selezionato anche il contatore selezionato dall'utente nel grafico a linee e nell'istogramma. In questo modo l'utente di Monitoraggio di sistema può visualizzare più facilmente il contatore selezionato quando vengono visualizzati diversi valori del contatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





