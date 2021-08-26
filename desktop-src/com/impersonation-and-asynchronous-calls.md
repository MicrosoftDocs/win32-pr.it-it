---
title: Rappresentazione e chiamate asincrone
description: Rappresentazione e chiamate asincrone
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84f7fcbdc820b50ef4eaaedd81ac579fcce64f1371bc57219348f6dcbedc0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070881"
---
# <a name="impersonation-and-asynchronous-calls"></a>Rappresentazione e chiamate asincrone

Il server non può rappresentare il client dopo il completamento della chiamata del server a [**ISynchronize::Signal,**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) anche se il metodo Begin non \_ è ancora stato completato. Si supponga, ad esempio, che un client chiami il metodo Begin, che il server elava immediatamente la chiamata e che il server chiami Signal per indicare che l'elaborazione è \_ stata completata.  Anche se il lavoro rimane da eseguire nel metodo Begin, il server non può rappresentare il client al termine della chiamata \_ a **Signal.**

Se il server rappresenta il client prima di chiamare [**Signal,**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)il token di rappresentazione non verrà rimosso dal thread fino a quando il server non chiama [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) o fino a quando non viene restituita la chiamata del server a Begin, a seconda di quale venga \_ prima.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Delega e rappresentazione](delegation-and-impersonation.md)
</dt> <dt>

[Esecuzione di una chiamata asincrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 