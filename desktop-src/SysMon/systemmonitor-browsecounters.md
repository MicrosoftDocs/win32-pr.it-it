---
title: Metodo SystemMonitor BrowseCounters
description: Consente di visualizzare la finestra di dialogo Aggiungi contatori .
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Metodo BrowseCounters SysMon
- Metodo BrowseCounters SysMon , interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon , metodo BrowseCounters
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e88d493ea0e4e1a9312191533162c8eb5a94cfb4233d17d21bb7217a136d403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882927"
---
# <a name="systemmonitorbrowsecounters-method"></a>Metodo SystemMonitor::BrowseCounters

Consente di visualizzare **la finestra di dialogo** Aggiungi contatori .

## <a name="syntax"></a>Sintassi


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa finestra di dialogo consente all'utente di selezionare contatori delle prestazioni locali o remoti da un elenco di oggetti prestazioni. I contatori selezionati vengono aggiunti alla raccolta [**Counters**](counters.md) e visualizzati nel grafico o nel report.

Per ricevere una notifica quando viene aggiunto un contatore, implementare [**l'evento OnCounterAdded.**](systemmonitor-oncounteradded.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**Counters.Add**](counters-add.md)
</dt> </dl>

 

 





