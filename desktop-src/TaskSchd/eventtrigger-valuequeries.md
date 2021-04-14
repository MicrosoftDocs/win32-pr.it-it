---
title: EventTrigger. ValueQueries, proprietà
description: Per la creazione di script, ottiene o imposta una raccolta di query XPath denominate. Ogni query della raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella proprietà di sottoscrizione.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Utilità di pianificazione proprietà ValueQueries
- Utilità di pianificazione proprietà ValueQueries, oggetto EventTrigger
- Utilità di pianificazione oggetto EventTrigger, proprietà ValueQueries
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
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518508"
---
# <a name="eventtriggervaluequeries-property"></a>EventTrigger. ValueQueries, proprietà

Per la creazione di script, ottiene o imposta una raccolta di query XPath denominate. Ogni query della raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella proprietà di [**sottoscrizione**](eventtrigger-subscription.md) .

## <a name="syntax"></a>Sintassi


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Valore proprietà

Raccolta di coppie nome-valore. Ogni coppia nome-valore nella raccolta definisce un nome univoco per il valore di una proprietà dell'evento che attiva il trigger di evento. Il valore della proprietà dell'evento viene definito come una query di eventi XPath. Per ulteriori informazioni sulle query di eventi XPath, vedere [Selezione eventi](/previous-versions//aa385231(v=vs.85)).

## <a name="remarks"></a>Commenti

Il nome della query può essere utilizzato come variabile nelle proprietà dell'azione seguenti:

-   [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md)
-   [**ShowMessageAction. title**](showmessageaction-title.md)
-   [**ExecAction. Arguments**](execaction-arguments.md)
-   [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md)
-   [**EmailAction. Server**](emailaction-server.md)
-   [**EmailAction. Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**EmailAction. Ccn**](emailaction-bcc.md)
-   [**EmailAction. ReplyTo**](emailaction-replyto.md)
-   [**EmailAction. from**](emailaction-from.md)
-   [**EmailAction. Body**](emailaction-body.md)
-   [**ComHandlerAction. Data**](comhandleraction-data.md)

Le stringhe di esempio di codice seguenti mostrano due coppie nome/valore che possono essere usate in una raccolta di valori di nome. I valori restituiti dalle query XPath possono sostituire le variabili nella proprietà di un'azione. Ai valori viene fatto riferimento in base al nome, con `$(user)` e `$(machine)` , nella proprietà Action. Se, ad esempio, `$(user)` le `$(machine)` variabili e vengono utilizzate nella stringa [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md) , il valore delle query XPath sostituisce le variabili nella stringa.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Per ulteriori informazioni sulla scrittura di una stringa di query per determinati eventi, vedere [selezione](/previous-versions//aa385231(v=vs.85)) di eventi e [sottoscrizione degli eventi](../wes/subscribing-to-events.md).

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
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

