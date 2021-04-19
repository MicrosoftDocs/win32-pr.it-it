---
description: Windows Sockets 1,1 ha introdotto il meccanismo di selezione asincrona per fornire indicazioni relative agli eventi di rete che non implicavano il polling o il blocco.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Messaggi di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308870"
---
# <a name="windows-messages"></a>Messaggi di Windows

Windows Sockets 1,1 ha introdotto il meccanismo di selezione asincrona per fornire indicazioni relative agli eventi di rete che non implicavano il polling o il blocco. La funzione [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) viene usata per registrare un interesse in uno o più eventi di rete, come elencato nell'esempio precedente, e fornire un handle di finestra da usare per la notifica. Quando si verifica un evento di rete denominato, viene inviato un messaggio di Windows specificato dal client alla finestra indicata. Per eseguire questa operazione, il provider di servizi deve usare la funzione [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) .

In Windows questo potrebbe non essere il meccanismo di notifica più efficiente ed è poco pratico per i daemon e i servizi che non vogliono aprire alcuna finestra. Per risolvere il problema, è stato introdotto il meccanismo di segnalazione degli oggetti evento descritto nella seguente procedura.

 

 
