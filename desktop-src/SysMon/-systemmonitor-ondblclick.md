---
title: Evento SystemMonitor. OnDblClick
description: Invia una notifica quando un utente fa doppio clic sulla linea del grafico, sulla barra istogramma o sull'elemento del report con il pulsante sinistro del mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Evento OnDblClick SysMon
- Evento OnDblClick SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnDblClick
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
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119875"
---
# <a name="systemmonitorondblclick-event"></a>Evento SystemMonitor. OnDblClick

Invia una notifica quando un utente fa doppio clic sulla linea del grafico, sulla barra istogramma o sull'elemento del report con il pulsante sinistro del mouse.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in uscita\]
</dt> <dd>

Indice del contatore selezionato nell'oggetto raccolta dei [**contatori**](counters.md) . Se non è stato selezionato alcun contatore, viene restituito un valore di indice pari a 0. in caso contrario, viene restituito l'indice del contatore selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando viene generato questo evento, nel riquadro Legenda viene selezionato anche il contatore selezionato dall'utente nel grafico a linee e nell'istogramma. In questo modo è più semplice per l'utente del monitor di sistema verificare quale contatore è selezionato quando vengono visualizzati diversi valori dei contatori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





