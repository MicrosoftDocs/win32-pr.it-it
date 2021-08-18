---
title: ShowMessageAction.MessageBody - proprietà
description: Per lo scripting, ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Proprietà MessageBody Utilità di pianificazione
- Proprietà MessageBody Utilità di pianificazione, oggetto ShowMessageAction
- Oggetto ShowMessageAction Utilità di pianificazione proprietà , MessageBody
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5b408ad8642cc17b85d783a8f26d7de3322a26309897e4d9b3c128401449d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139344"
---
# <a name="showmessageactionmessagebody-property"></a>ShowMessageAction.MessageBody - proprietà

\[Questo oggetto non è più supportato. È possibile usare IExecAction con la Windows di scripting [**msgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.\]

Per lo scripting, ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.

## <a name="syntax"></a>Sintassi


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Valore proprietà

Testo del messaggio visualizzato nel corpo della finestra di messaggio.

## <a name="remarks"></a>Commenti

Le stringhe con parametri possono essere utilizzate nel testo del messaggio della finestra di messaggio. Per altre informazioni, vedere la sezione Esempi in [**EventTrigger.ValueQueries.**](eventtrigger-valuequeries.md)

Quando si imposta il valore di questa proprietà, il valore può essere testo recuperato da una risorsa .dll file. Una stringa specializzata viene usata per fare riferimento al testo dal file di risorse. Il formato della stringa è $(@ Dll , ResourceID ) dove Dll è il percorso del file .dll che contiene la risorsa e ResourceID è l'identificatore per il testo \[ \] della \[ \] \[ \] \[ \] risorsa. Ad esempio, l'impostazione del valore di questa proprietà su $(@ %SystemRoot% System32ResourceName.dll, -101) imposta la proprietà sul valore del testo della risorsa con un identificatore uguale a \\ \\ -101 nel file diResourceName.dll %SystemRoot% \\ System32. \\

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                    |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

