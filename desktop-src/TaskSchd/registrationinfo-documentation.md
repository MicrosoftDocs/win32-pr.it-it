---
title: RegistrationInfo.Docproprietà umentation
description: Per la creazione di script, ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- Utilità di pianificazione proprietà documentazione
- Utilità di pianificazione proprietà della documentazione, oggetto RegistrationInfo
- Utilità di pianificazione oggetto RegistrationInfo, Proprietà Documentation
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
ms.openlocfilehash: 5832c78fae5c0ee9629077693db7e283369cc8af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118930"
---
# <a name="registrationinfodocumentation-property"></a>RegistrationInfo.Docproprietà umentation

Per la creazione di script, ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.

## <a name="syntax"></a>Sintassi


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a>Valore proprietà

Documentazione aggiuntiva associata all'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, la documentazione aggiuntiva per l'attività viene specificata utilizzando l'elemento [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) dello schema utilità di pianificazione.

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

 

 





