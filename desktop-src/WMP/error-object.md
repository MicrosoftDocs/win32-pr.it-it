---
title: Oggetto Error (WMP SDK)
description: L'oggetto Error fornisce l'accesso a una raccolta di oggetti ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Finestra oggetto errore Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/09/2019
ms.locfileid: "106299317"
---
# <a name="error-object"></a>Oggetto Error

L'oggetto **Error** fornisce l'accesso a una raccolta di oggetti [ErrorItem](erroritem-object.md) .

L'oggetto **Error** supporta la proprietà seguente.



| Proprietà                           | Descrizione                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | Recupera il numero di errori nella coda degli errori. |



 

L'oggetto **Error** supporta i metodi seguenti.



| Metodo                                       | Descrizione                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearErrorQueue](error-clearerrorqueue.md) | Cancella gli errori dalla coda degli errori.                                                         |
| [item](error-item.md)                       | Recupera un oggetto [ErrorItem](erroritem-object.md) dalla coda degli errori.                     |
| [webHelp](error-webhelp.md)                 | Avvia la pagina della Guida di Windows Media Player Web per visualizzare altre informazioni sull'errore. |



 

È possibile accedere all'oggetto **errore** tramite la proprietà seguente.



| Oggetto                      | Proprietà                  |
|-----------------------------|---------------------------|
| [Player](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




