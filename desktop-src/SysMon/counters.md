---
title: Raccolta di contatori (Isysmon.h)
description: Usare questa classe per gestire la raccolta di oggetti CounterItem. Per recuperare questo oggetto, chiamare SystemMonitor.Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Raccolta di contatori SysMon
- Raccolta di contatori SysMon , descritta
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
ms.openlocfilehash: f8349c1425450491c3fc658f6ac1ac3c5fcf75d3e617a92f6e34b91f2f5802e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883338"
---
# <a name="counters-collection"></a>Raccolta di contatori

Usare questa classe per gestire la raccolta di [**oggetti CounterItem.**](counteritem.md)

Per recuperare questo oggetto, chiamare [**SystemMonitor.Counters**](systemmonitor-counters.md).

## <a name="members"></a>Membri

La **raccolta Counters** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **raccolta Counters** include questi metodi.



| Metodo                            | Descrizione                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Aggiungere**](counters-add.md)       | Aggiunge [**un'istanza CounterItem**](counteritem.md) alla raccolta.<br/>      |
| [**Rimuovi**](counters-remove.md) | Rimuove [**un'istanza CounterItem**](counteritem.md) dalla raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

La **raccolta Counters** ha queste proprietà.



| Proprietà                                   | Descrizione                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Conteggio**](counters-count.md)<br/> | Recupera il numero di [**istanze CounterItem**](counteritem.md) nella raccolta.<br/>  |
| [**Elemento**](counters-item.md)<br/>   | Recupera l'istanza [**counterItem**](counteritem.md) specificata dalla raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

**L'oggetto Counters** è la proprietà predefinita dell'oggetto [**SystemMonitor.**](systemmonitor.md)

Aggiungere a questa raccolta i contatori di cui si vuole eseguire il grafo. SYSMON recupera i valori dei contatori dal sistema o da un file di log a seconda [**dell'origine**](systemmonitor-datasourcetype.md) dati specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





