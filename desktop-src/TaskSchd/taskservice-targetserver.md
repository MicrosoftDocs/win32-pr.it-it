---
title: Proprietà TaskService. TargetServer
description: Per gli script, ottiene il nome del computer in cui è in esecuzione il Utilità di pianificazione servizio a cui è connesso l'utente.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Utilità di pianificazione proprietà TargetServer
- Utilità di pianificazione proprietà TargetServer, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, proprietà TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519094"
---
# <a name="taskservicetargetserver-property"></a>Proprietà TaskService. TargetServer

Per gli script, ottiene il nome del computer in cui è in esecuzione il Utilità di pianificazione servizio a cui è connesso l'utente.

## <a name="syntax"></a>Sintassi


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Valore proprietà

Nome del computer che esegue il servizio Utilità di pianificazione a cui è connesso l'utente.

## <a name="remarks"></a>Commenti

Questa proprietà restituisce una stringa vuota quando l'utente passa un indirizzo IP, localhost o ' .' come parametro e restituisce il nome del computer che esegue il servizio Utilità di pianificazione quando l'utente non passa alcun valore di parametro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





