---
description: ICE44 verifica che NewDialog, SpawnDialog e SpawnWaitDialog ControlEvents fanno riferimento a finestre di dialogo valide nella tabella Dialog.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ee7bb074ec2dcc395cdf17750e2ab1b0364026e0f949c9b9e3f2589a8b59261
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581011"
---
# <a name="ice44"></a>ICE44

ICE44 verifica che [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)e [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents fanno riferimento a finestre di dialogo valide nella [tabella Dialog](dialog-table.md).

## <a name="result"></a>Risultato

ICE44 invia un messaggio di errore se è presente un evento di controllo della finestra di dialogo che non fa riferimento a una finestra di dialogo elencata nella tabella Dialog.

## <a name="example"></a>Esempio

ICE44 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE44                                                                                                                               | Descrizione                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento di controllo per il controllo 'Dialog1'. Control1' è di tipo SpawnDialog, ma il relativo argomento Dialog2 non è una voce valida nella tabella finestre di dialogo. | Sono presenti azioni SpawnDialog, SpawnWaitDialog o NewDialog con un argomento che non fa riferimento a una finestra di dialogo nella tabella Dialog. Per correggere l'errore, aggiungere un argomento che rappresenta una chiave nella tabella della finestra di dialogo.<br/> |



 

[Tabella delle finestre](dialog-table.md) di dialogo (parziale)



| Finestra di dialogo  | Titolo |
|---------|-------|
| Finestra di dialogo1 |       |



 

[Tabella ControlEvent](controlevent-table.md) (parziale)



| Finestra di dialogo\_ | controllo\_ | Tipo        | Argomento |
|----------|-----------|-------------|----------|
| Finestra di dialogo1  | Control1  | SpawnDialog | Finestra di dialogo2  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




