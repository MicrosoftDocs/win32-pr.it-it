---
title: Proprietà ShowMessageAction. MessageBody
description: Per lo scripting, ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Utilità di pianificazione proprietà MessageBody
- Utilità di pianificazione proprietà MessageBody, oggetto ShowMessageAction
- Oggetto ShowMessageAction Utilità di pianificazione, Proprietà MessageBody
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
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873489"
---
# <a name="showmessageactionmessagebody-property"></a>Proprietà ShowMessageAction. MessageBody

\[Questo oggetto non è più supportato. È possibile utilizzare IExecAction con la funzione Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.\]

Per lo scripting, ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.

## <a name="syntax"></a>Sintassi


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Valore proprietà

Testo del messaggio visualizzato nel corpo della finestra di messaggio.

## <a name="remarks"></a>Commenti

Le stringhe con parametri possono essere utilizzate nel testo del messaggio della finestra di messaggio. Per ulteriori informazioni, vedere la sezione Esempi in [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).

Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll. Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse. Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa. Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                    |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

