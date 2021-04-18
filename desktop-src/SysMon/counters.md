---
title: Raccolta dei contatori (Isysmon. h)
description: Utilizzare questa classe per gestire la raccolta di oggetti CounterItem. Per recuperare l'oggetto, chiamare SystemMonitor. Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- SysMon raccolta contatori
- Raccolta di contatori SysMon, descritti
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302249"
---
# <a name="counters-collection"></a>Raccolta di contatori

Utilizzare questa classe per gestire la raccolta di oggetti [**CounterItem**](counteritem.md) .

Per recuperare l'oggetto, chiamare [**SystemMonitor. Counters**](systemmonitor-counters.md).

## <a name="members"></a>Membri

La raccolta di **contatori** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La raccolta di **contatori** presenta questi metodi.



| Metodo                            | Descrizione                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Aggiungere**](counters-add.md)       | Aggiunge un'istanza di [**CounterItem**](counteritem.md) alla raccolta.<br/>      |
| [**Rimuovi**](counters-remove.md) | Rimuove un'istanza di [**CounterItem**](counteritem.md) dalla raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

La raccolta di **contatori** dispone di queste proprietà.



| Proprietà                                   | Descrizione                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Conteggio**](counters-count.md)<br/> | Recupera il numero di istanze di [**CounterItem**](counteritem.md) nell'insieme.<br/>  |
| [**Elemento**](counters-item.md)<br/>   | Recupera l'istanza di [**CounterItem**](counteritem.md) specificata dalla raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

L'oggetto **contatori** è la proprietà predefinita dell'oggetto [**SystemMonitor**](systemmonitor.md) .

Aggiungere a questa raccolta i contatori che si desidera rappresentare nel grafico. SYSMON recupera i valori del contatore dal sistema o da un file di log a seconda dell' [**origine dati**](systemmonitor-datasourcetype.md) specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





