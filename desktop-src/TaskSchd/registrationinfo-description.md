---
title: RegistrationInfo.Description - proprietà
description: Per lo scripting, ottiene o imposta la descrizione dell'attività.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Proprietà Description Utilità di pianificazione
- Proprietà Description Utilità di pianificazione, oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione proprietà , Description
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
ms.openlocfilehash: ea6f141eddc40b21f1cf49e490fe30df5844e6029f821d9811b0e62ea55fa8ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872461"
---
# <a name="registrationinfodescription-property"></a>RegistrationInfo.Description - proprietà

Per lo scripting, ottiene o imposta la descrizione dell'attività.

## <a name="syntax"></a>Sintassi


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a>Valore proprietà

Descrizione dell'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, la descrizione dell'attività viene specificata utilizzando l'elemento [**Description**](taskschedulerschema-description-registrationinfotype-element.md) dello schema Utilità di pianificazione.

Quando si imposta il valore di questa proprietà, il valore può essere testo recuperato da una risorsa .dll file. Una stringa specializzata viene usata per fare riferimento al testo dal file di risorse. Il formato della stringa è $(@ Dll , ResourceID ) dove Dll è il percorso del file .dll che contiene la risorsa e ResourceID è l'identificatore per il testo \[ \] della \[ \] \[ \] \[ \] risorsa. Ad esempio, l'impostazione del valore di questa proprietà su $(@ %SystemRoot% System32ResourceName.dll, -101) imposta la proprietà sul valore del testo della risorsa con un identificatore uguale a \\ \\ -101 nel file diResourceName.dll %SystemRoot% \\ System32. \\

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





