---
title: Proprietà TaskSettings. NetworkSettings
description: Per gli script, ottiene o imposta l'oggetto impostazioni di rete che contiene un identificatore e un nome del profilo di rete.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Utilità di pianificazione proprietà NetworkSettings
- Utilità di pianificazione proprietà NetworkSettings, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà NetworkSettings
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
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740426"
---
# <a name="tasksettingsnetworksettings-property"></a>Proprietà TaskSettings. NetworkSettings

Per gli script, ottiene o imposta l'oggetto impostazioni di rete che contiene un identificatore e un nome del profilo di rete. Se la proprietà [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) di [**TaskSettings**](tasksettings.md) è **true** e un propfile di rete viene specificato nella proprietà **NetworkSettings** , l'attività verrà eseguita solo se il profilo di rete specificato è disponibile.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**NetworkSettings**](networksettings.md) che contiene un identificatore e un nome del profilo di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





