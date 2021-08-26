---
title: RegistrationInfo.Source - proprietà
description: Per lo scripting, ottiene o imposta l'origine dell'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Proprietà di origine Utilità di pianificazione
- Proprietà source Utilità di pianificazione, oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione proprietà Source
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
ms.openlocfilehash: 97320d63823599e52327533afdba62f795622263e57878515ddd7ade9c98070b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126031"
---
# <a name="registrationinfosource-property"></a>RegistrationInfo.Source - proprietà

Per lo scripting, ottiene o imposta l'origine dell'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.

## <a name="syntax"></a>Sintassi


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>Valore proprietà

Origine dell'attività. Ad esempio, da un componente, un servizio, un'applicazione o un utente.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, le informazioni sull'origine dell'attività vengono specificate utilizzando [**l'elemento Source**](taskschedulerschema-source-registrationinfotype-element.md) dello schema Utilità di pianificazione attività.

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

 

 





