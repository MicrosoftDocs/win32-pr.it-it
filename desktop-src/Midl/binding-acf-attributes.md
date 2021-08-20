---
title: Associazione di attributi ACF
description: Specificare la modalità di connessione del client al server per le chiamate di procedura remota con gli attributi elencati nella tabella seguente.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF MIDL, attributi, associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32b4d53cea81ed2a69a702a1a58942834a538ffbef75cb11315dd792882bf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385227"
---
# <a name="binding-acf-attributes"></a>Associazione di attributi ACF

Specificare la modalità di connessione del client al server per le chiamate di procedura remota con gli attributi elencati nella tabella seguente.



| Attributo                                                          | Utilizzo                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)                                             | Definisce un handle che consente al chiamante di effettuare una chiamata asincrona e di restituire immediatamente senza attendere i risultati e quindi di risincronizzare con la funzione chiamata per ricevere i dati al termine della chiamata. |
| [**handle \_ automatico**](auto-handle.md)                                | Indica a MIDL di consentire al codice stub di controllare automaticamente l'associazione. Si tratta dell'impostazione predefinita se non si specifica alcun handle di associazione.                                                                                    |
| [**context \_ handle \_ noserialize**](context-handle-noserialize.md) | Garantisce che un handle di contesto non verrà mai serializzato, indipendentemente dal comportamento predefinito dell'applicazione.                                                                                                       |
| [**serializzazione \_ dell'handle \_ di contesto**](context-handle-serialize.md)     | Garantisce che un handle di contesto verrà sempre serializzato, indipendentemente dal comportamento predefinito dell'applicazione                                                                                                       |
| [**handle \_ esplicito**](explicit-handle.md)                        | Consente all'applicazione client di controllare l'associazione con un parametro esplicito in ogni procedura.                                                                                                                      |
| [**handle \_ implicito**](implicit-handle.md)                        | Specifica un handle per le routine che non dispongono di un parametro handle esplicito. L'applicazione client controlla ancora l'associazione.                                                                                |
| [**handle \_ di contesto \_ strict**](strict-context-handle.md)           | Garantisce che i metodi nell'interfaccia accettino solo handle di contesto creati da un metodo di tale interfaccia.                                                                                     |



 

 

 




