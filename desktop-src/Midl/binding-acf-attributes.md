---
title: Associazione di attributi ACF
description: Specificare il modo in cui il client si connette al server per le chiamate di procedure remote con gli attributi elencati nella tabella seguente.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- MIDL, attributi, associazione di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045112"
---
# <a name="binding-acf-attributes"></a>Associazione di attributi ACF

Specificare il modo in cui il client si connette al server per le chiamate di procedure remote con gli attributi elencati nella tabella seguente.



| Attributo                                                          | Utilizzo                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)                                             | Definisce un handle che consente al chiamante di eseguire una chiamata asincrona e di restituire immediatamente un valore senza attendere i risultati, quindi di eseguire nuovamente la sincronizzazione con la funzione chiamata per ricevere i dati al termine della chiamata. |
| [**\_handle automatico**](auto-handle.md)                                | Indica a MIDL di consentire al codice dello stub di controllare automaticamente l'associazione. Si tratta dell'impostazione predefinita se non si specifica alcun handle di associazione.                                                                                    |
| [**gestore del contesto \_ \_ noserialize**](context-handle-noserialize.md) | Garantisce che un handle di contesto non verrà mai serializzato, indipendentemente dal comportamento predefinito dell'applicazione.                                                                                                       |
| [**\_serializzazione handle di contesto \_**](context-handle-serialize.md)     | Garantisce che un handle di contesto venga sempre serializzato, indipendentemente dal comportamento predefinito dell'applicazione                                                                                                       |
| [**handle esplicito \_**](explicit-handle.md)                        | Consente all'applicazione client di controllare l'associazione con un parametro esplicito in ogni routine.                                                                                                                      |
| [**handle implicito \_**](implicit-handle.md)                        | Specifica un handle per le routine che non dispongono di un parametro di handle esplicito. L'applicazione client controlla ancora l'associazione.                                                                                |
| [**\_handle di contesto Strict \_**](strict-context-handle.md)           | Garantisce che i metodi dell'interfaccia accettino solo handle di contesto creati da un metodo di tale interfaccia.                                                                                     |



 

 

 




