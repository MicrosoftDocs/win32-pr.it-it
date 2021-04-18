---
description: WSPEventSelect si comporta esattamente come WSPAsyncSelect, ad eccezione del fatto che, anziché causare l'invio di un messaggio di Windows al verificarsi di qualsiasi evento di rete FD xxx designato, \_ ad esempio FD \_ Read, FD \_ Write e così via, viene impostato un oggetto evento designato.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Segnalazione di oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306988"
---
# <a name="event-object-signaling"></a>Segnalazione di oggetti evento

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) si comporta esattamente come [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , ad eccezione del fatto che, anziché causare l'invio di un messaggio di Windows al verificarsi di qualsiasi evento di rete FD xxx designato, \_ ad esempio FD \_ Read, FD \_ Write e così via, viene impostato un oggetto evento designato.

Inoltre, il fatto che si \_ sia verificato un evento di rete FD XXX specifico viene memorizzato dal provider di servizi. Questa operazione è necessaria perché l'occorrenza di tutti gli eventi di rete nominati comporterà la segnalazione di un singolo oggetto evento. Una chiamata a [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) causa la copia del contenuto corrente della memoria degli eventi di rete in un buffer fornito dal client e la memoria degli eventi di rete da cancellare. Il client può inoltre designare un particolare oggetto evento da cancellare atomicamente insieme alla memoria dell'evento di rete.

 

 
