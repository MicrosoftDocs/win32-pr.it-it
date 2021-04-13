---
title: Proprietà RegistrationInfo. Description
description: Per la creazione di script, ottiene o imposta la descrizione dell'attività.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Proprietà Description Utilità di pianificazione
- Descrizione Utilità di pianificazione proprietà, oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione, proprietà Description
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c79b60fe6a96493c52011e5bd731679b3fee1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400206"
---
# <a name="registrationinfodescription-property"></a>Proprietà RegistrationInfo. Description

Per la creazione di script, ottiene o imposta la descrizione dell'attività.

## <a name="syntax"></a>Sintassi


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a>Valore proprietà

Descrizione dell'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, la descrizione dell'attività viene specificata utilizzando l'elemento [**Description**](taskschedulerschema-description-registrationinfotype-element.md) dello schema utilità di pianificazione.

Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll. Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse. Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa. Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





