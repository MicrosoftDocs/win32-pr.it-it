---
title: EventTrigger.ValueQueries - proprietà
description: Per lo scripting, ottiene o imposta una raccolta di query XPath denominate. Ogni query nella raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella proprietà Subscription.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Proprietà ValueQueries Utilità di pianificazione
- Proprietà ValueQueries Utilità di pianificazione , oggetto EventTrigger
- EventTrigger object Utilità di pianificazione , ValueQueries property
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8fd28cd616af56a9b51ecf4e709df5f07674c6d1f307320128645364f3bfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253881"
---
# <a name="eventtriggervaluequeries-property"></a>EventTrigger.ValueQueries - proprietà

Per lo scripting, ottiene o imposta una raccolta di query XPath denominate. Ogni query nella raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella [**proprietà Subscription.**](eventtrigger-subscription.md)

## <a name="syntax"></a>Sintassi


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Valore proprietà

Raccolta di coppie nome-valore. Ogni coppia nome-valore nella raccolta definisce un nome univoco per un valore di proprietà dell'evento che attiva il trigger di evento. Il valore della proprietà dell'evento è definito come query di eventi XPath. Per altre informazioni sulle query di evento XPath, vedere [Selezione di eventi](/previous-versions//aa385231(v=vs.85)).

## <a name="remarks"></a>Commenti

Il nome della query può essere usato come variabile nelle proprietà dell'azione seguenti:

-   [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md)
-   [**ShowMessageAction.Title**](showmessageaction-title.md)
-   [**ExecAction.Arguments**](execaction-arguments.md)
-   [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md)
-   [**EmailAction.Server**](emailaction-server.md)
-   [**EmailAction.Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**EmailAction.Bcc**](emailaction-bcc.md)
-   [**EmailAction.ReplyTo**](emailaction-replyto.md)
-   [**EmailAction.From**](emailaction-from.md)
-   [**EmailAction.Body**](emailaction-body.md)
-   [**ComHandlerAction.Data**](comhandleraction-data.md)

Le stringhe di esempio di codice seguenti mostrano due coppie nome-valore che possono essere usate in una raccolta nome-valore. I valori restituiti dalle query XPath possono sostituire le variabili nella proprietà di un'azione. Ai valori viene fatto riferimento in base al nome, `$(user)` con e , nella proprietà `$(machine)` dell'azione. Ad esempio, se le variabili e vengono usate nella stringa `$(user)` `$(machine)` [**ShowMessageAction.MessageBody,**](showmessageaction-messagebody.md) il valore delle query XPath sostituirà le variabili nella stringa.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Per altre informazioni sulla scrittura di una stringa di query per determinati eventi, [vedere](/previous-versions//aa385231(v=vs.85)) Selezione e sottoscrizione di eventi [.](../wes/subscribing-to-events.md)

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
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

