---
title: Proprietà RegistrationInfo. Source
description: Per gli script, ottiene o imposta la posizione da cui ha origine l'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Utilità di pianificazione proprietà di origine
- Utilità di pianificazione proprietà di origine, oggetto RegistrationInfo
- Utilità di pianificazione oggetto RegistrationInfo, proprietà Source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742442"
---
# <a name="registrationinfosource-property"></a>Proprietà RegistrationInfo. Source

Per gli script, ottiene o imposta la posizione da cui ha origine l'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.

## <a name="syntax"></a>Sintassi


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>Valore proprietà

Da cui ha origine l'attività. Ad esempio, da un componente, un servizio, un'applicazione o un utente.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, le informazioni sull'origine dell'attività vengono specificate utilizzando l'elemento di [**origine**](taskschedulerschema-source-registrationinfotype-element.md) dello schema di utilità di pianificazione.

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

 

 





