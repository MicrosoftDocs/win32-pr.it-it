---
title: RegistrationInfo.Documentation
description: Per lo scripting, ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- Proprietà documentation Utilità di pianificazione
- Proprietà Documentation Utilità di pianificazione , oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione proprietà , Documentation
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31878417d6a225c5fa7c67569d557a4c6d7a716a24bffd94dfe58a84e3809a37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100181"
---
# <a name="registrationinfodocumentation-property"></a>RegistrationInfo.Documentation

Per lo scripting, ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.

## <a name="syntax"></a>Sintassi


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a>Valore proprietà

Qualsiasi documentazione aggiuntiva associata all'attività.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, la documentazione aggiuntiva per l'attività viene specificata usando l'elemento [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) dello schema Utilità di pianificazione attività.

Quando si imposta il valore di questa proprietà, il valore può essere testo recuperato da una risorsa .dll file. Viene usata una stringa specializzata per fare riferimento al testo del file di risorse. Il formato della stringa è $(@ Dll , ResourceID ) dove Dll è il percorso del file .dll che contiene la risorsa e ResourceID è l'identificatore per il testo \[ \] della \[ \] \[ \] \[ \] risorsa. Ad esempio, l'impostazione di questo valore della proprietà su $(@ %SystemRoot% System32ResourceName.dll, -101) imposta la proprietà sul valore del testo della risorsa con un identificatore uguale a \\ \\ -101 nel file diResourceName.dll %SystemRoot% \\ System32. \\

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





