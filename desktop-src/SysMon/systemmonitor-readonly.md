---
title: Proprietà SystemMonitor. ReadOnly
description: Recupera o imposta un valore che determina se un utente può modificare i valori delle proprietà del controllo.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Proprietà di sola lettura SysMon
- Proprietà ReadOnly SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964179"
---
# <a name="systemmonitorreadonly-property"></a>Proprietà SystemMonitor. ReadOnly

Recupera o imposta un valore che determina se un utente può modificare i valori delle proprietà del controllo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a>Valore proprietà

True se non si desidera che l'utente modifichi i valori delle proprietà del controllo; in caso contrario, false. Il valore predefinito è false, ovvero gli utenti possono modificare i valori delle proprietà del controllo.

## <a name="remarks"></a>Commenti

Quando il valore di questa proprietà è true, vengono applicate le condizioni seguenti:

-   L'utente non può utilizzare il menu di scelta rapida.
-   I seguenti pulsanti della barra degli strumenti sono disabilitati:
    -   Nuovo insieme di contatori
    -   Visualizza attività corrente
    -   Visualizzazione dei dati dei file di log
    -   Add
    -   Delete
    -   Incolla elenco contatori
    -   Proprietà

Si noti che questa proprietà ha effetto solo sulla capacità dell'utente di modificare i valori delle proprietà tramite l'interfaccia utente, ma non impedisce di modificare a livello di codice i valori delle proprietà o i contatori.

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

 

 





