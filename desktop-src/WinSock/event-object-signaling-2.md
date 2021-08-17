---
description: WSPEventSelect si comporta esattamente come WSPAsyncSelect, ad eccezione del fatto che, anziché inviare un messaggio Windows in caso di evento di rete FD XXX designato (ad esempio FD READ, FD WRITE e così via), viene impostato un oggetto evento \_ \_ \_ designato.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Segnalazione di oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eed237db696298a2f8053fb61cb0009d9d25d7f37497e0a19d58044d27d8dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132623"
---
# <a name="event-object-signaling"></a>Segnalazione di oggetti evento

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) si comporta esattamente come [**WSPAsyncSelect,**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) ad eccezione del fatto che, anziché inviare un messaggio Windows in caso di evento di rete FD XXX designato (ad esempio FD READ, FD WRITE e così via), viene impostato un oggetto evento \_ \_ \_ designato.

Inoltre, il provider di servizi ricorda che si è verificato un particolare evento di rete FD \_ XXX. Questa operazione è necessaria perché l'occorrenza di tutti gli eventi di rete nominati comporta la segnalazione di un singolo oggetto evento. Una chiamata a [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) determina la copia del contenuto corrente della memoria degli eventi di rete in un buffer fornito dal client e la memoria degli eventi di rete da cancellare. Il client può anche designare un particolare oggetto evento da cancellare atomicamente insieme alla memoria degli eventi di rete.

 

 
