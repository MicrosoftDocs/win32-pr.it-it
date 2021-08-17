---
title: TaskSettings.NetworkSettings - proprietà
description: Per lo scripting, ottiene o imposta l'oggetto impostazioni di rete che contiene un identificatore e un nome del profilo di rete.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Proprietà NetworkSettings Utilità di pianificazione
- Proprietà NetworkSettings Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione , proprietà NetworkSettings
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730701c71a69f05b73524d6f9d1d8ad3d89b5e93620664be33a80c5c41af1479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059658"
---
# <a name="tasksettingsnetworksettings-property"></a>TaskSettings.NetworkSettings - proprietà

Per lo scripting, ottiene o imposta l'oggetto impostazioni di rete che contiene un identificatore e un nome del profilo di rete. Se la [**proprietà RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) di [**TaskSettings**](tasksettings.md) è **True** e nella proprietà **NetworkSettings** è specificato un propfile di rete, l'attività verrà eseguita solo se il profilo di rete specificato è disponibile.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**NetworkSettings**](networksettings.md) che contiene un identificatore e un nome del profilo di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





