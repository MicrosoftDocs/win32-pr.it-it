---
title: Client multithreading e handle di contesto
description: Quando si dispone di un client multithreading in cui più thread utilizzano la stessa istanza dell'handle di contesto, per impostazione predefinita l'accesso all'istanza dell'handle di contesto viene serializzato nel server.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c621d75d8cc48ca1f71719066f455e0efce39f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047057"
---
# <a name="multithreaded-clients-and-context-handles"></a>Client multithreading e handle di contesto

Quando si dispone di un client multithreading in cui più thread utilizzano la stessa istanza dell'handle di contesto, per impostazione predefinita l'accesso all'istanza dell'handle di contesto viene serializzato nel server. In questo modo si evita che Server Manager debba proteggersi da un altro thread dello stesso client che modifica il contesto o il contesto che si sta esaurendo durante l'invio di una chiamata. In alcuni casi, tuttavia, la serializzazione può avere un effetto sulle prestazioni.

Tenere presente quanto segue: due thread client richiamano una chiamata di procedura remota che non modifica lo stato del contesto (ad esempio, la chiamata ottiene semplicemente alcuni valori da esso). Tali chiamate non devono essere serializzate.

Per tali situazioni, Windows XP offre un modello di serializzazione in modalità mista, in cui ogni metodo può essere dichiarato per avere accesso esclusivo o condiviso a un handle di contesto. Per informazioni dettagliate, vedere Gestione del contesto [ \_ \_ serializzazione](/windows/desktop/Midl/context-handle-serialize) e [gestione del contesto \_ \_ noserialize](/windows/desktop/Midl/context-handle-noserialize) .

Nelle versioni di Windows precedenti a Windows XP, l'unico mezzo per consentire l'accesso simultaneo a un handle di contesto consiste nel chiamare la funzione [**RpcSsDontSerializeContext**](/previous-versions/aa378473(v=vs.80)) per consentire l'invio di più chiamate in un singolo handle di contesto. La chiamata della funzione **RpcSsDontSerializeContext** non disabilita completamente la serializzazione. Quando si verifica un errore di esecuzione del contesto, la routine di esecuzione del contesto viene eseguita solo quando tutte le richieste client in attesa sono state completate. Una chiamata a **RpcScDontSerializeContext** influiscono sull'intero processo e non è ripristinabile. Non è consigliabile usare **RpcScDontSerializeContext** in Windows XP e versioni successive. rende il codice server molto complesso quando si gestiscono in modo affidabile con Race condition inerenti a ambienti completamente non serializzati.

 

 