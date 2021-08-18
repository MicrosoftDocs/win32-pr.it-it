---
title: Client multithreading e handle di contesto
description: Quando si dispone di un client multithreading in cui più thread usano la stessa istanza dell'handle di contesto, l'accesso all'istanza dell'handle di contesto viene serializzato nel server per impostazione predefinita.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7fed15deacca47754f51869fa0b18b37135586addb7f80b8aa75b9dde63082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928087"
---
# <a name="multithreaded-clients-and-context-handles"></a>Client multithreading e handle di contesto

Quando si dispone di un client multithreading in cui più thread usano la stessa istanza dell'handle di contesto, l'accesso all'istanza dell'handle di contesto viene serializzato nel server per impostazione predefinita. In questo modo, il server manager non deve proteggersi da un altro thread dello stesso client che modifica il contesto o il contesto in esecuzione durante l'invio di una chiamata. Tuttavia, in alcuni casi la serializzazione può influire sulle prestazioni.

Si consideri quanto segue: due thread client richiamano una chiamata di procedura remota che non modifica lo stato del contesto (ad esempio, la chiamata ottiene semplicemente alcuni valori da esso). Tali chiamate non devono essere serializzate.

In questi casi, Windows XP offre un modello di serializzazione in modalità mista, in cui ogni metodo può essere dichiarato per avere accesso esclusivo o condiviso a un handle di contesto. Per [informazioni \_ \_ dettagliate, vedere serializzazione dell'handle](/windows/desktop/Midl/context-handle-serialize) di contesto e handle di contesto [ \_ \_ noserialize.](/windows/desktop/Midl/context-handle-noserialize)

Nelle versioni di Windows precedenti Windows XP, l'unico modo per consentire l'accesso simultaneo a un handle di contesto è chiamare la funzione [**RpcSsDontSerializeContext**](/previous-versions/aa378473(v=vs.80)) per consentire l'invio di più chiamate in un singolo handle di contesto. La chiamata **alla funzione RpcSsDontSerializeContext** non disabilita completamente la serializzazione. Quando si verifica un run-down del contesto, la routine di esecuzione del contesto viene eseguita solo quando tutte le richieste client in sospeso sono state completate. Una chiamata a **RpcScDontSerializeContext influisce** sull'intero processo e non è ripristinabile. Non **è consigliabile usare RpcScDontSerializeContext** in Windows XP e versioni successive. rende il codice server molto complicato quando si gestiscono in modo affidabile le race conditions intrinseche in ambienti completamente non serializzati.

 

 