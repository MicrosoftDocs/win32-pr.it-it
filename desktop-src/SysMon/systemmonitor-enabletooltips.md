---
title: Proprietà SystemMonitor. EnableToolTips
description: Recupera o imposta un valore che determina se viene visualizzata una descrizione comandi quando il puntatore del mouse viene posizionato su un contatore in una delle visualizzazioni del grafico (non supportato per la visualizzazione report).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Proprietà EnableToolTips SysMon
- Proprietà EnableToolTips SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà EnableToolTips
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301695"
---
# <a name="systemmonitorenabletooltips-property"></a>Proprietà SystemMonitor. EnableToolTips

Recupera o imposta un valore che determina se viene visualizzata una descrizione comandi quando il puntatore del mouse viene posizionato su un contatore in una delle visualizzazioni del grafico (non supportato per la visualizzazione report).

## <a name="syntax"></a>Sintassi


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a>Valore proprietà

True Visualizza una descrizione comando contenente le informazioni sul contatore; in caso contrario, false.

## <a name="remarks"></a>Commenti

Per i grafici a linee, la descrizione comando è ancorata al punto dati più vicino al mouse. Per i grafici a barre e gli istogrammi, la descrizione comando rappresenta il valore totale dei dati della barra, non un punto all'interno della barra.

La descrizione comando contiene informazioni diverse in base all'origine dati. Per i file di log, la descrizione comando contiene il percorso del contatore, il valore del contatore, il timestamp, il numero di campioni di dati inclusi nel punto dati e i valori di dati minimo e massimo.

Per l'attività in tempo reale, la descrizione comando contiene il percorso del contatore, il valore del contatore e il timestamp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





