---
description: ICE44 verifica che NewDialog, SpawnDialog e SpawnWaitDialog ControlEvents facciano riferimento a finestre di dialogo valide nella tabella della finestra di dialogo.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314212"
---
# <a name="ice44"></a>ICE44

ICE44 verifica che [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)e [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents facciano riferimento a finestre di dialogo valide nella [tabella della finestra di dialogo](dialog-table.md).

## <a name="result"></a>Risultato

ICE44 Invia un messaggio di errore se è presente un evento di controllo della finestra di dialogo che non fa riferimento a una finestra di dialogo elencata nella tabella della finestra di dialogo.

## <a name="example"></a>Esempio

ICE44 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE44                                                                                                                               | Descrizione                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento di controllo per il controllo ' Dialog1' .' Control1' è di tipo SpawnDialog, ma il relativo argomento Dialog2 non è una voce valida nella tabella della finestra di dialogo. | Sono presenti azioni SpawnDialog, SpawnWaitDialog o NewDialog con un argomento che non fa riferimento a una finestra di dialogo nella tabella della finestra di dialogo. Per correggere l'errore, aggiungere un argomento che rappresenta una chiave nella tabella della finestra di dialogo.<br/> |



 

[Tabella finestra di dialogo](dialog-table.md) (parziale)



| Finestra di dialogo  | Titolo |
|---------|-------|
| Dialog1 |       |



 

[Tabella ControlEvent](controlevent-table.md) (parziale)



| Finestra di dialogo\_ | controllo\_ | Tipo        | Argomento |
|----------|-----------|-------------|----------|
| Dialog1  | Control1  | SpawnDialog | Dialog2  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




