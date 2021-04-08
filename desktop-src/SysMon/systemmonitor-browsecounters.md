---
title: Metodo SystemMonitor BrowseCounters
description: Consente di visualizzare la finestra di dialogo Aggiungi contatori.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Metodo BrowseCounters SysMon
- Metodo BrowseCounters SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, metodo BrowseCounters
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
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047820"
---
# <a name="systemmonitorbrowsecounters-method"></a>Metodo SystemMonitor:: BrowseCounters

Consente di visualizzare la finestra di dialogo **Aggiungi contatori** .

## <a name="syntax"></a>Sintassi


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa finestra di dialogo consente all'utente di selezionare i contatori delle prestazioni locali o remoti da un elenco di oggetti prestazioni. I contatori selezionati vengono aggiunti alla raccolta dei [**contatori**](counters.md) e visualizzati nel grafico o nel report.

Per ricevere una notifica quando viene aggiunto un contatore, implementare l'evento [**OnCounterAdded**](systemmonitor-oncounteradded.md) .

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

[**Contatori. Aggiungi**](counters-add.md)
</dt> </dl>

 

 





