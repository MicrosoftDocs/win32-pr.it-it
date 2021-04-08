---
title: Rappresentazione e chiamate asincrone
description: Rappresentazione e chiamate asincrone
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730679"
---
# <a name="impersonation-and-asynchronous-calls"></a>Rappresentazione e chiamate asincrone

Il server non può rappresentare il client dopo che la chiamata del server a [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) è stata completata, anche se il \_ metodo Begin non è stato ancora completato. Si supponga, ad esempio, che un client chiami il \_ metodo Begin, il server elabori immediatamente la chiamata e il server chiami **Signal** per indicare che l'elaborazione è terminata. Anche se il lavoro continua a essere eseguito nel \_ metodo Begin, il server non può rappresentare il client al termine della chiamata a **Signal** .

Se il server rappresenta il client prima di chiamare il [**segnale**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), il token di rappresentazione non verrà rimosso dal thread finché il server non chiamerà [**IServerSecurity:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) o fino a quando non viene effettuata la chiamata al server per iniziare \_ , a seconda di quale si verifichi per primo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Delega e rappresentazione](delegation-and-impersonation.md)
</dt> <dt>

[Esecuzione di una chiamata asincrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 