---
title: Oggetto Error (WMP SDK)
description: L'oggetto Error fornisce l'accesso a una raccolta di oggetti ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Errore dell'Windows Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c8e5b7627db2c55eb41a267f6c8d3a7a779e2f20190ca3061a49a41eb8577adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748470"
---
# <a name="error-object"></a>Oggetto Error

**L'oggetto Error** fornisce l'accesso a una raccolta [di oggetti ErrorItem.](erroritem-object.md)

**L'oggetto Error** supporta la proprietà seguente.



| Proprietà                           | Descrizione                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | Recupera il numero di errori nella coda degli errori. |



 

**L'oggetto Error** supporta i metodi seguenti.



| Metodo                                       | Descrizione                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearErrorQueue](error-clearerrorqueue.md) | Cancella gli errori dalla coda degli errori.                                                         |
| [item](error-item.md)                       | Recupera un [oggetto ErrorItem](erroritem-object.md) dalla coda degli errori.                     |
| [Webhelp](error-webhelp.md)                 | Avvia la pagina Windows Media Player Guida Web per visualizzare altre informazioni sull'errore. |



 

**L'accesso** all'oggetto Error viene eseguito tramite la proprietà seguente.



| Oggetto                      | Proprietà                  |
|-----------------------------|---------------------------|
| [Player](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




